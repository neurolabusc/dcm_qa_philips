## About

dcm_qa_philips is a simple DICOM to NIfTI validator script and dataset. This repository is similar to [dcm_qa](https://github.com/neurolabusc/dcm_qa), but includes data from Philips MRI scanners.

## License

Data origin is described in the `notes.txt` file for each series. The the code and images are covered by the [2-clause BSD license](https://opensource.org/licenses/BSD-2-Clause).

## Versions

24-February-2019
 - Initial public release

## Running

Assuming that the executable dcm2niix is in your path, you should be able to simply run the script `batch.sh` from the terminal.

If you have problems you can edit the first few lines of the `batch.sh` script so that `basedir` reports the explicit location of the `dcm_qa` folder (by default this is assumed to be the folder containing the script) on your computer and `exenam` reports the explicit location of dcm2niix (by default it is assumed to be in your path). Also, make sure the script is executable (`chmod +x batch.sh`). Then run the script.

## Updating dcm_qa_philips

This software reports when there are any changes in behavior of the software. However, some of these changes might be improvements. For example, software which supports future BIDS tags will report differences relative to the prior solutions reported in dcm_qa_philips. Once the solutions have been verified as correct, one needs to update both dcm_qa_philips and the software that invokes dcm_qa_philips. For example, with dcm2niix we can update it to use the latest version of dcm_qa with this script:

```
cd dcm2niix
git submodule update --remote
git commit -am 'Update dcm_qa_philips submodule.'
git push
```

## Useful Links

 - dcm2niix's handling of these files is described [here](https://github.com/rordenlab/dcm2niix/tree/master/Philips).

