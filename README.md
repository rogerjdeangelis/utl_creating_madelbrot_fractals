# utl_creating_madelbrot_fractals
Creating Madelbrot Fractals Keywords: sas sql join merge big data analytics macros oracle teradata mysql sas communities stackoverflow statistics artificial inteligence AI Python R Java Javascript WPS Matlab SPSS Scala Perl C C# Excel MS Access JSON graphics maps NLP natural language processing machine learning igraph DOSUBL DOW loop stackoverflow SAS community.

    Creating Madelbrot Fractals

    Output:  Be patient when viewing the gif(3 minute video?)
    see output
    https://goo.gl/kBvhjL
    https://github.com/rogerjdeangelis/utl_creating_madelbrot_fractals/blob/master/utl_creating_madelbrot_fractals.gif

    see
    https://communities.sas.com/t5/Base-SAS-Programming/mandelbrot-program/m-p/426501

    Other solutions

    see  (for detailed documentation)
    https://dreamtolearn.com/ryan/data_analytics_viz/23

    https://goo.gl/55oXdK
    https://www.google.com/search?q=r+create+mandelbrot&oq=r+create+mandelbrot&aqs=chrome..69i57j69i64.13313j0j8&sourceid=chrome&ie=UTF-


    Self contained input, process and output

    %utl_submit_wps64('
    options set=R_HOME "C:/Program Files/R/R-3.3.2";
    libname wrk sas7bdat "%sysfunc(pathname(work))";
    proc r;
    submit;
    source("C:/Program Files/R/R-3.3.2/etc/Rprofile.site", echo=T);
    library(caTools);
    jet.colors <- colorRampPalette(c("#00007F", "blue", "#007FFF", "cyan", "#7FFF7F",
       "yellow", "#FF7F00", "red", "#7F0000"));
    m <- 800;
    C <- complex( real=rep(seq(-1.8,0.6, length.out=m), each=m ),
                  imag=rep(seq(-1.2,1.2, length.out=m), m ) );
    C <- matrix(C,m,m);
    Z <- 0;
    X <- array(0, c(m,m,20));
    for (k in 1:10) {
      Z <- Z^2+C;
      X[,,k] <- exp(-abs(Z));
    };
    write.gif(X, "d:/gif/utl_creating_madelbrot_fractals.gif", col=jet.colors, delay=1000);
    endsubmit;
    ');

