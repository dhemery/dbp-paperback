require 'rake/clean'

slug = 'example'
fmt_name = 'dbp'

tex_file = "#{slug}.tex"
pdf_file = "#{slug}.pdf"
log_file = "#{slug}.log"

task default: :show

file pdf_file => tex_file do |t|
  `pdftex -fmt #{fmt_name} #{tex_file}`
end

desc 'Typeset the book as a PDF file'
task build: pdf_file

desc 'Show the PDF file'
task show: :build do
  `open #{pdf_file}`
end

CLEAN << pdf_file
CLEAN << log_file
