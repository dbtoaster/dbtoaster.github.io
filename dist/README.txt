RELEASE INFORMATION


----------------
Release 2.2 (revision 3387) - 2015/11/27

Frontend: svn update -r3387 (svn update -r3393)
Backend: git checkout e6ac66537265873b20525f8fc5f46449fd9877e1

Requirements:
    gcc version 4.9.4 (MacPorts gcc49 4.9.4_2) 
    boost 1.50.0 (should be removed)
    The OCaml toplevel, version 4.02.2
    ruby 1.8.7 (2013-06-27 patchlevel 374) [i686-darwin16]

Quick test:
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -c q3
    (Linux/Mac) scala -cp ./q3.jar:./lib/dbt_scala/* ddbt.gen.Dbtoaster
    (Windows) scala -cp "./q3.jar;./lib/dbt_scala/dbtoaster_2.10-2.2-lms.jar;./lib/dbt_scala/dbtoaster-shared_2.10-1.0.jar" ddbt.gen.Dbtoaster

    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -c q3
    ./q3

Regression test:
    unit -v -x -xsc -xvm -p 2 -w 0 -s 1 -l scala -l cpp -q tpch.* -q simple.*

----------------
Release 2.1 (revision 3346) - 2014/11/06

Frontend: svn update -r3346 (svn update -r3350)
Backend: git checkout 1189618c0855a85753743969ba4de31f540b9d1c

Requirements:
    gcc version 4.9.4 (MacPorts gcc49 4.9.4_2) 
    boost 1.50.0 (should be removed)
    The OCaml toplevel, version 4.02.2
    ruby 1.8.7 (2013-06-27 patchlevel 374) [i686-darwin16]

Quick test:
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -c q3
    (Linux/Mac) scala -cp ./q3.jar:./lib/dbt_scala/* ddbt.gen.Dbtoaster
    (Windows) scala -cp "./q3.jar;./lib/dbt_scala/dbtoaster_2.10-2.1-lms.jar" ddbt.gen.Dbtoaster

    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -c q3
    ./q3

Regression test:
    unit -v -x -xsc -xvm -p 2 -w 0 -s 1 -l scala -l cpp -q tpch.* -q simple.*

----------------
Release 2 (revision 3263) - 2014/08/01

Frontend: svn update -r3263 (svn update -r3295)
Backend: git checkout 066fb4646e3f1f05842f21a424471f03b49221e2

Requirements:
    gcc version 4.9.4 (MacPorts gcc49 4.9.4_2) 
    boost 1.50.0 (should be removed)
    The OCaml toplevel, version 4.02.2
    ruby 1.8.7 (2013-06-27 patchlevel 374) [i686-darwin16]

Quick test:
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -c q3
    scala -cp ./q3.jar:./lib/dbt_scala/* ddbt.gen.Dbtoaster
    (Windows) scala -cp "./q3.jar;./lib/dbt_scala/dbtoaster_2.10-2.1-lms.jar" ddbt.gen.Dbtoaster

    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -c q3
    ./q3

Regression test:
    unit -v -x -xsc -xvm -p 2 -w 0 -s 1 -l scala -l cpp -q tpch.* -q simple.*

----------------
Release 1 (revision 2827) - 2013/02/11

svn update -r2827

Requirements:
    gcc45 libgcc45  gcc version 4.5.4 (MacPorts gcc45 4.5.4_13) 
    boost 1.50.0
        sudo ./bootstrap.sh --prefix=/Users/milllic/Temp/boost --with-libraries=program_options,serialization,system,filesystem,chrono,thread
        sudo ./b2 install
    Objective Caml version 3.12.1
    ruby 1.8.7 (2013-06-27 patchlevel 374) [i686-darwin16]

Quick test:
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -c q3
    scala -cp ./q3.jar:./lib/dbt_scala/dbtlib.jar org.dbtoaster.RunQuery
    (Windows) scala -cp "./q3.jar;./lib/dbt_scala/dbtlib.jar" org.dbtoaster.RunQuery

    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -c q3 -I /Users/milllic/Temp/boost/include -L /Users/milllic/Temp/boost/lib 
    export DYLD_LIBRARY_PATH=/Users/milllic/Temp/boost/lib
    ./q3

----------------
Beta for Release 1 (revision 2525) - 2012/07/19

svn update -r2525

Requirements:
    gcc45 libgcc45  gcc version 4.5.4 (MacPorts gcc45 4.5.4_13) 
    boost 1.50.0
        sudo ./bootstrap.sh --prefix=/Users/milllic/Temp/boost --with-libraries=program_options,serialization,system,filesystem,chrono,thread
        sudo ./b2 install
    Objective Caml version 3.12.1
    ruby 1.8.7 (2013-06-27 patchlevel 374) [i686-darwin16]

Quick test:
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l scala examples/queries/tpch/query3.sql -c q3
    scala -cp ./q3.jar:./lib/dbt_scala/dbtlib.jar org.dbtoaster.RunQuery
    (Windows) scala -cp "./q3.jar;./lib/dbt_scala/dbtlib.jar" org.dbtoaster.RunQuery

    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -r
    bin/dbtoaster -O3 -l cpp examples/queries/tpch/query3.sql -c q3 -I /Users/milllic/Temp/boost/include -L /Users/milllic/Temp/boost/lib 
    export DYLD_LIBRARY_PATH=/Users/milllic/Temp/boost/lib
    ./q3

----------------