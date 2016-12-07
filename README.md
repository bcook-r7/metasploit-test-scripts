Meterpreter System Test
==
The idea here is to provide some system way to automatically test
Meterpreter and Metasploit together automatically, putting both through
their paces without a lot of manual intervention.

Prerequisites
--

This assumes you have vagrant installed and some vagrant boxes installed
matching the names in the 'oses' file. Your vagrant boxes should have
ssh access. For Windows testing, I am using these packer templates to
generate the test VMs:

https://github.com/joefitzgerald/packer-windows

Running
--

 - Import your vagrant boxes into your test machine's environment, e.g.

```
vagrant box add -name windows_2012_r2 /srv/media/vagrant-boxes/windows_2012_r2_virtualbox.box
```

 - Add your box's name to the 'oses' file.
 - Add the payload types you wish to test to the 'payloads' file.
 - Run 'run-tests'
