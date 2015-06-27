require 'rake/clean'

CLEAN.include '*.aux'
CLEAN.include '*.log'

task :default => ['poster.pdf', 'surface.dat', 'mcmc.dat', 'hmc.dat']
CLOBBER.include 'poster.pdf'

rule '.pdf' => '.tex' do |t|
  sh "pdflatex #{t.source}"
end
