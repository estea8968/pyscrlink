#!/bin/bash

usage() {
	echo "Usage: ${0} COMMAND"
	echo -e "COMMAND:"
	echo -e "\tbuild"
	echo -e "\tupload-testpypi FILES"
	exit 1
}

case ${1} in
	build)
		python3 setup.py sdist bdist_wheel
		;;
	upload)
		shift
		python3 -m twine upload "$@"
		;;
	upload-testpypi)
		shift
		python3 -m twine upload --repository testpypi "$@"
		;;
	*)
		usage
		;;
esac
