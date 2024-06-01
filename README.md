This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/ck).

*Check [CM MLPerf docs](https://mlcommons.github.io/inference) for more details.*

## Host platform

* OS version: Linux-5.15.0-1046-nvidia-x86_64-with-glibc2.35
* CPU version: x86_64
* Python version: 3.10.12 (main, Nov 20 2023, 15:14:05) [GCC 11.4.0]
* MLCommons CM version: 2.3.1

## CM Run Command

See [CM installation guide](https://github.com/mlcommons/ck/blob/master/docs/installation.md).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo gateoverflow@cm4mlops --checkout=c48f3835e53c98d10387d8f06f54008159a07e45

cm run script \
	--tags=run-mlperf,inference \
	--model=sdxl \
	--implementation=reference \
	--backend=pytorch \
	--device=cuda \
	--precision=float32 \
	--scenario=Offline \
	--quiet
```
*Note that if you want to use the [latest automation recipes](https://access.cknowledge.org/playground/?action=scripts) for MLPerf (CM scripts),
 you should simply reload gateoverflow@cm4mlops without checkout and clean CM cache as follows:*

```bash
cm rm repo gateoverflow@cm4mlops
cm pull repo gateoverflow@cm4mlops
cm rm cache -f

```# MlPerfLogExample
