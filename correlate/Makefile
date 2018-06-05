init:
	( \
	sudo python2 -m pip install virtualenv; \
	python2 -m virtualenv -p python2 venv; \
	)

venv: venv/bin/activate
venv/bin/activate: requirements.txt
	( \
	test -d venv || virtualenv venv; \
	venv/bin/pip install -Ur requirements.txt; \
	touch venv/bin/activate; \
	)

devbuild: venv
	( \
	venv/bin/python -m pip install -r requirements.txt \
	)

#test: devbuild
#	venv/bin/python test/runtests.py;
