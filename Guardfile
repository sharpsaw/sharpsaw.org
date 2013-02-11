guard 'shell' do
  watch /.*index.haml$/ do |m|
    input = m.first
    output = input.sub /haml$/, 'html'
    "haml #{input} > #{output}\n" + `haml #{input} > #{output}`
  end
end
