# 500R23D1P5U

Measurement setup with Class 2 lever and a non-inverted cam, for the purpose of investigating the effect of input voltage.

Use the specialized notebook to generate statistics:

```
$ cd bpsim_home/meas/1.0
$ for p in $(pwd)/500R23D1P5U/*.{1,2,3}.txt; do cam-bpw-sim import-optoforce --fs 333 $p 1.0/500R23D1P5U; done
$ cam-bpw-sim meas-val 1.0/500R23D1P5U/P5_*.{1,2,3}.m.hdf5
$ cam-bpw-sim meas-val-summary 1.0/500R23D1P5U/meas_vs_cam --notebook $(pwd)/500R23D1P5U/fcr_waveform_summary_voltage.ipynb
```
