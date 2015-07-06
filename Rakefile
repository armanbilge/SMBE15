require 'rake/clean'

CLEAN.include '*.aux'
CLEAN.include '*.log'

task :default => 'poster.pdf'

file 'poster.pdf' => ['poster.tex', 'surface.dat', 'mcmc.dat', 'hmc.dat', 'performance.dat', 'uoa.tex', 'awc.tex']
CLOBBER.include 'poster.pdf'

rule '.pdf' => '.tex' do |t|
  sh "pdflatex --shell-escape #{t.source}"
end
