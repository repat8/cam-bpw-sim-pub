- Use the contents of `./.config/cam-bpw-sim/config.toml` to fill the auto-generated file created by the command line command `cam-bpw-sim init-config`.
- Edit the variable `simulator_home` to point to the real location of `./bpsim_home` folder on your computer.
- Data can be processed with `cam-bpw-sim`.

For example:

```
$ cd bpsim_home/meas/1.0
$ for p in $(pwd)/500R23D1C2/*.{1,2,3}.txt; do cam-bpw-sim import-optoforce --fs 333 $p 1.0/500R23D1C2; done
$ for p in $(pwd)/500R23D1C1/*.{1,2,3}.txt; do cam-bpw-sim import-optoforce --fs 333 $p 1.0/500R23D1C1; done
$ cam-bpw-sim meas-val 1.0/*/P5_*.{1,2,3}.m.hdf5
$ cam-bpw-sim meas-val-summary 1.0/500R23D1{C2,C1}/meas_vs_cam
```
