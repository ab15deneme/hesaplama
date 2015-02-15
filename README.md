
# Python ve Bilimsel Hesaplama

###### *Bu dokÃ¼man aÃ§Ä±k kaynak, Ã¶zgÃ¼r yazÄ±lÄ±m ruhuyla yazÄ±lmÄ±ÅŸtÄ±r. <br> Akademik
BiliÅŸim ile olan baÄŸÄ±nÄ± koparmadan istediÄŸiniz gibi kullanabilirsiniz.* ######

## KarÅŸÄ±laÅŸma

Python' u kurduk.

                1.6.1 Linux
In Ubuntu Linux, to installing python and all the requirements run:
$ sudo apt-get install python ipython ipython-notebook
$ sudo apt-get install python-numpy python-scipy python-matplotlib python-sympy
$ sudo apt-get install spyder
1.6.2 MacOS X
Macports
Python is included by default in Mac OS X, but for our purposes it will be useful to install a new python
environment using Macports, because it makes it much easier to install all the required additional packages.
Using Macports, we can install what we need with:
$ sudo port install py27-ipython +pyside+notebook+parallel+scientific
$ sudo port install py27-scipy py27-matplotlib py27-sympy
$ sudo port install py27-spyder
These will associate the commands python and ipython with the versions installed via macports (instead
of the one that is shipped with Mac OS X), run the following commands:
$ sudo port select python python27
$ sudo port select ipython ipython27
Fink
Or, alternatively, you can use the Fink package manager. After installing Fink, use the following command
to install python and the packages that we need:
$ sudo fink install python27 ipython-py27 numpy-py27 matplotlib-py27 scipy-py27 sympy-py27
$ sudo fink install spyder-mac-py27
1.6.3 Windows
Windows lacks a good packaging system, so the easiest way to setup a Python environment is to install a
pre-packaged distribution. Some good alternatives are:
 Enthought Python Distribution. EPD is a commercial product but is available free for academic use.
 Anaconda CE. Anaconda Pro is a commercial product, but Anaconda Community Edition is free.
 Python(x,y). Fully open source.
Note EPD and Anaconda CE are also available for Linux and Max OS X.
                
Python arayÃ¼zÃ¼nÃ¼ aÃ§tÄ±k.

                Ipython' u tercih ediyoruz;
To start IPython in the notebook mode, open up the terminal (Linux) and type the following command in Linux:
$ipython notebook --pylab inline
or, on MS Windows open the DOS Prompt by going to the WIndows Start > Run and entering cmd.exe and choosing OK. This will open the DOS Prompt and there type the followingcommand:
>ipython notebook --pylab inline
Mac
Letâ€™s just make sure that ipynb actually runs now. To do so, simply execute the following command in the terminal:

$ ipython-2.7 notebook
                
ArtÄ±k kader aÄŸlarÄ±nÄ± Ã¶rebilir

## TanÄ±ÅŸma

Ä°lk komutumuz ekrana yazÄ± yazdÄ±rma;


    print "Merhaba DÃ¼nya"

    Merhaba DÃ¼nya
    

Hemen konuya girelim. Derdimiz hesaplama. Komut SatÄ±rÄ±nÄ± Ã¶nce hesap makinesi
gibi kullanalÄ±m.


    3 + .14




    3.14




    2015 - 115 + 7




    1907



HesaplarÄ±mÄ±zÄ± bir deÄŸiÅŸken yardÄ±mÄ±yla da yapabiliriz


    a = 5


    a * a




    25




    b = a**2


    b




    25



Ä°ÅŸlemler iÃ§iÃ§e de yapÄ±labilir


    2**2**2




    16



Ä°ÅŸlem Ã¶nceliklerine dikkat!


    2**2**2 + 2 / 2




    17



Parantez kullanmakta yarar var


    2**(2**2) + (2 / 2)




    17



Bunlar bize yetmez. FarklÄ± matematik iÅŸlemler yapmak iÃ§in **math** modÃ¼lÃ¼nden
yararlanalÄ±m. <br>
(*Python' da kullanabileceÄŸiniz bir Ã§ok Ã¶zellik ve fonksiyon modÃ¼ller ile
sunulur. Bu modÃ¼lleri ÅŸu aÅŸamada hazÄ±r kÃ¼tÃ¼phaneler gibi dÃ¼ÅŸÃ¼nebilirsiniz.
**math** modÃ¼lÃ¼nÃ¼ ilk Ã¶nce *import* komutu ile Ã§alÄ±ÅŸma alanÄ±mÄ±za dahil
edeceÄŸiz.*)

import math

Åimdi iÃ§indeki fonksiyonlara ulaÅŸabiliriz. Ã–nce neler var bakalÄ±m;


    dir(math)




    ['__doc__',
     '__name__',
     '__package__',
     'acos',
     'acosh',
     'asin',
     'asinh',
     'atan',
     'atan2',
     'atanh',
     'ceil',
     'copysign',
     'cos',
     'cosh',
     'degrees',
     'e',
     'erf',
     'erfc',
     'exp',
     'expm1',
     'fabs',
     'factorial',
     'floor',
     'fmod',
     'frexp',
     'fsum',
     'gamma',
     'hypot',
     'isinf',
     'isnan',
     'ldexp',
     'lgamma',
     'log',
     'log10',
     'log1p',
     'modf',
     'pi',
     'pow',
     'radians',
     'sin',
     'sinh',
     'sqrt',
     'tan',
     'tanh',
     'trunc']



BazÄ±larÄ± tanÄ±dÄ±k ama biraz yardÄ±m iyi olur;


    help(math)

    Help on built-in module math:
    
    NAME
        math
    
    FILE
        (built-in)
    
    DESCRIPTION
        This module is always available.  It provides access to the
        mathematical functions defined by the C standard.
    
    FUNCTIONS
        acos(...)
            acos(x)
            
            Return the arc cosine (measured in radians) of x.
        
        acosh(...)
            acosh(x)
            
            Return the hyperbolic arc cosine (measured in radians) of x.
        
        asin(...)
            asin(x)
            
            Return the arc sine (measured in radians) of x.
        
        asinh(...)
            asinh(x)
            
            Return the hyperbolic arc sine (measured in radians) of x.
        
        atan(...)
            atan(x)
            
            Return the arc tangent (measured in radians) of x.
        
        atan2(...)
            atan2(y, x)
            
            Return the arc tangent (measured in radians) of y/x.
            Unlike atan(y/x), the signs of both x and y are considered.
        
        atanh(...)
            atanh(x)
            
            Return the hyperbolic arc tangent (measured in radians) of x.
        
        ceil(...)
            ceil(x)
            
            Return the ceiling of x as a float.
            This is the smallest integral value >= x.
        
        copysign(...)
            copysign(x, y)
            
            Return x with the sign of y.
        
        cos(...)
            cos(x)
            
            Return the cosine of x (measured in radians).
        
        cosh(...)
            cosh(x)
            
            Return the hyperbolic cosine of x.
        
        degrees(...)
            degrees(x)
            
            Convert angle x from radians to degrees.
        
        erf(...)
            erf(x)
            
            Error function at x.
        
        erfc(...)
            erfc(x)
            
            Complementary error function at x.
        
        exp(...)
            exp(x)
            
            Return e raised to the power of x.
        
        expm1(...)
            expm1(x)
            
            Return exp(x)-1.
            This function avoids the loss of precision involved in the direct evaluation of exp(x)-1 for small x.
        
        fabs(...)
            fabs(x)
            
            Return the absolute value of the float x.
        
        factorial(...)
            factorial(x) -> Integral
            
            Find x!. Raise a ValueError if x is negative or non-integral.
        
        floor(...)
            floor(x)
            
            Return the floor of x as a float.
            This is the largest integral value <= x.
        
        fmod(...)
            fmod(x, y)
            
            Return fmod(x, y), according to platform C.  x % y may differ.
        
        frexp(...)
            frexp(x)
            
            Return the mantissa and exponent of x, as pair (m, e).
            m is a float and e is an int, such that x = m * 2.**e.
            If x is 0, m and e are both 0.  Else 0.5 <= abs(m) < 1.0.
        
        fsum(...)
            fsum(iterable)
            
            Return an accurate floating point sum of values in the iterable.
            Assumes IEEE-754 floating point arithmetic.
        
        gamma(...)
            gamma(x)
            
            Gamma function at x.
        
        hypot(...)
            hypot(x, y)
            
            Return the Euclidean distance, sqrt(x*x + y*y).
        
        isinf(...)
            isinf(x) -> bool
            
            Check if float x is infinite (positive or negative).
        
        isnan(...)
            isnan(x) -> bool
            
            Check if float x is not a number (NaN).
        
        ldexp(...)
            ldexp(x, i)
            
            Return x * (2**i).
        
        lgamma(...)
            lgamma(x)
            
            Natural logarithm of absolute value of Gamma function at x.
        
        log(...)
            log(x[, base])
            
            Return the logarithm of x to the given base.
            If the base not specified, returns the natural logarithm (base e) of x.
        
        log10(...)
            log10(x)
            
            Return the base 10 logarithm of x.
        
        log1p(...)
            log1p(x)
            
            Return the natural logarithm of 1+x (base e).
            The result is computed in a way which is accurate for x near zero.
        
        modf(...)
            modf(x)
            
            Return the fractional and integer parts of x.  Both results carry the sign
            of x and are floats.
        
        pow(...)
            pow(x, y)
            
            Return x**y (x to the power of y).
        
        radians(...)
            radians(x)
            
            Convert angle x from degrees to radians.
        
        sin(...)
            sin(x)
            
            Return the sine of x (measured in radians).
        
        sinh(...)
            sinh(x)
            
            Return the hyperbolic sine of x.
        
        sqrt(...)
            sqrt(x)
            
            Return the square root of x.
        
        tan(...)
            tan(x)
            
            Return the tangent of x (measured in radians).
        
        tanh(...)
            tanh(x)
            
            Return the hyperbolic tangent of x.
        
        trunc(...)
            trunc(x:Real) -> Integral
            
            Truncates x to the nearest Integral toward 0. Uses the __trunc__ magic method.
    
    DATA
        e = 2.718281828459045
        pi = 3.141592653589793
    
    
    

ArtÄ±k birÅŸeyler deneyelim.


    math.asin(0.5) # ModÃ¼l iÃ§indeki fonksiyon ve deÄŸiÅŸkenlere bu ÅŸekilde ulaÅŸÄ±yorum modÃ¼lismi.fonksiyonismi()




    0.5235987755982989



30 bekliyorduk. Belli ki sonuÃ§ radyan cinsinden. <br>
(*Ã–zel fonksiyonlar dÄ±ÅŸÄ±nda aÃ§Ä±lar radyan cinsinden kullanÄ±lÄ±r*)


    math.asin(0.5) / math.pi * 180




    30.000000000000004



Bunu 30 kabul edebiliriz sanÄ±rÄ±m ama bir tuhaflÄ±k var. Daha bildik birÅŸey
deneyelim


    math.sin(math.pi)




    1.2246467991473532e-16



?? <br>
(* 1.2246467991473532e-16 = $1.2246467991473532 * 10^{-16}$ *)

NoktalÄ± sayÄ±larda ufak bir arÄ±za mÄ± var? TamsayÄ±larda durum nasÄ±l?


    3/2  #Bu tamsayÄ± bÃ¶lÃ¼mÃ¼dÃ¼r. SonuÃ§ tamsayÄ± olur (sonuÃ§ en yakÄ±n tamsayÄ±ya yuvarlanÄ±r).




    1




    3.0 / 2  #Sonucun noktalÄ± sayÄ± olmasÄ±nÄ± istiyorsanÄ±z en az birini noktalÄ± deÄŸer olarak tanÄ±mlayÄ±n




    1.5




    float(3)/2  #float() fonksiyonu girilen sayÄ±yÄ± noktalÄ± sayÄ± yapar




    1.5




    int(3.0/2)  #int() fonksiyonu girilen sayÄ±yÄ± tamsayÄ± yapar




    1



SayÄ±larÄ± Ã§ok kurcalamayalÄ±m en iyisi. Biraz yazÄ± yazalÄ±m;


    metin = 'Akademik'


    print metin

    Akademik
    

Demek ki metinler tek tÄ±rnakla yazÄ±lÄ±yor


    print metin + " BiliÅŸim"

    Akademik BiliÅŸim
    

AyrÄ±ca Ã§ift tÄ±rnak da oluyormuÅŸ


    print metin + " BiliÅŸim" + ''' %i''' % 2015

    Akademik BiliÅŸim 2015
    

Peki peki biz sayÄ±lara geri dÃ¶nelim. Zaten sayÄ± kullanmadan bilimsel hesaplama
yapÄ±lÄ±r mÄ±? Hatta bana bir sÃ¼rÃ¼ sayÄ± lazÄ±m;


    a = [1, 2, 8, 4, 5]


    print a

    [1, 2, 8, 4, 5]
    

GÃ¼zel. YalnÄ±z 3. eleman sÄ±rayÄ± bozdu;


    a[3] = 3


    a




    [1, 2, 8, 3, 5]



Ä°lla bir cinslik olacak;


    a[2] = 3


    a




    [1, 2, 3, 3, 5]



NeymiÅŸ, indeks 0' dan baÅŸlÄ±yormuÅŸ. Sondan 2. yi de dÃ¼zeltelim;


    a[-2] = 4


    a




    [1, 2, 3, 4, 5]



Sondan indeks ise 1' den baÅŸlÄ±yor. <br>
Peki bir sayÄ±nÄ±n a sayÄ± dizisine ait olup olmadÄ±ÄŸÄ±na bakabilir miyiz?


    6 in a




    False



Daha aÃ§Ä±klayÄ±cÄ± bir cevap yazdÄ±rsak


    b = 6
    if b in a:
        print "b a' nÄ±n iÃ§inde var"  # metin iÃ§inde tÄ±rnak kullanmaya Ã¶rnek!
    else:
        print 'b a\' nÄ±n iÃ§inde yok' # bu da baÅŸka bir yÃ¶ntem
    

    b a' nÄ±n iÃ§inde yok
    

SÃ¶zdizimi (syntax) orjinalmiÅŸ yalnÄ±z. <br>
Daha ileri birÅŸey yapalÄ±m. a' nÄ±n bÃ¼tÃ¼n elemanlarÄ±nÄ±n mesela 2 katÄ±nÄ± bulalÄ±m


    for n in a:       # Her yinelemede (iteration) n deÄŸiÅŸkeni a' nÄ±n bir elemanÄ±nÄ±n deÄŸerini alacak ve  
        print n * 2   # for dÃ¶ngÃ¼sÃ¼ iÃ§indeki iÅŸlemler n' nin bu deÄŸeri ile Ã§alÄ±ÅŸtÄ±rÄ±lacak
    

    2
    4
    6
    8
    10
    

Bu da gÃ¼zel! <br>
SonuÃ§ olarak kÃ¶ÅŸeli parantez ile sayÄ± dizileri (vektÃ¶r, matris)
tanÄ±mlayabiliyoruz gibi gÃ¶rÃ¼nÃ¼yor <br>
YalnÄ±z a bildiÄŸimiz vektÃ¶rse eÄŸer, bu iÅŸlemi vektÃ¶r skaler Ã§arpÄ±mÄ± ÅŸeklinde
yapabilmeliyim


    b = a * 2
    b




    [1, 2, 3, 4, 5, 1, 2, 3, 4, 5]



Aa bu vektÃ¶r deÄŸil mi?


    a[0:2] = ['A', 'a'] #Ä°ndeksle nasÄ±l aralÄ±k tanÄ±mladÄ±ÄŸÄ±mÄ±za dikkat: baÅŸlangÄ±Ã§_indeksi:bitiÅŸ_indeksi-1
    a




    ['A', 'a', 3, 4, 5]



DeÄŸilmiÅŸ :( <br>
(*a deÄŸiÅŸkeni aslÄ±nda "List" veri tipindedir. "List" veri tipleri kÃ¶ÅŸeli
parantez ile tanÄ±mlananÄ±r ve deÄŸiÅŸik tipte verileri kabul eden diziler
oluÅŸturulmasÄ±nÄ± saÄŸlar (DiÄŸer bir deyiÅŸle homojen deÄŸildir. FarklÄ± tÃ¼rde
elemanlar iÃ§erebilir). Matematiksel iÅŸlemlerdeki sayÄ± dizileri iÃ§in Ã§ok uygun
deÄŸildir.*)

Peki ben kendi fonksiyonlarÄ±mÄ± yazmak istersem. Mesela hedehode diye bir
fonksiyonum olsun girilen deÄŸerin mod 10 daki deÄŸerinin 10 tabanÄ±nda
logaritmasÄ±nÄ± alsÄ±n


    def hedehode(a):
        b = a%10
        return math.log10(b)
    


    hedehode(1)




    0.0




    hedehode(10)


    ---------------------------------------------------------------------------
    ValueError                                Traceback (most recent call last)

    <ipython-input-39-333b65fa60ca> in <module>()
    ----> 1 hedehode(10)
    

    <ipython-input-37-71788d5e9772> in hedehode(a)
          1 def hedehode(a):
          2     b = a%10
    ----> 3     return math.log10(b)
    

    ValueError: math domain error


Kendi fonksiyonunu yazmak Ã¶yle kolay deÄŸil demek. Bilen de bilmeyen de
kullanÄ±yor.

## Muhabbeti KoyulaÅŸtÄ±ralÄ±m

Benim derdim sayÄ± dizileri ve onlarla olan iÅŸlemler. VektÃ¶r, matris, lineer
cebir, tÃ¼rev, vb. Yok mu bunlar iÃ§in birÅŸeyler?


    import numpy # Bu mudur?


    a = numpy.array([[1,2,3],[4, 5, 6]])
    a




    array([[1, 2, 3],
           [4, 5, 6]])




    a[1,0] # satir,sÃ¼tun => 2. satÄ±r, 1. sÃ¼tun (indeks 0' dan baÅŸlÄ±yor unutmayÄ±n)




    4




    b = a * 2
    b




    array([[ 2,  4,  6],
           [ 8, 10, 12]])



Ä°ÅŸte budur. Peki a' nÄ±n devriÄŸi(transpose) mesela


    b = a.T
    b




    array([[1, 4],
           [2, 5],
           [3, 6]])



Devam!


    b = a * a # eleman-eleman Ã§arpÄ±m, Ã¶r: b[1,1] = a[1,1] * a[1,1]

? (matris Ã§arpÄ±mÄ±?)


    numpy.dot(a, a.T) # 2 boyutlu diziler iÃ§in matris Ã§arpÄ±mÄ±




    array([[14, 32],
           [32, 77]])




    b = a[0,:]
    c = a[1,:]
    numpy.dot(b,c) # 1 boyutlu diziler iÃ§in iÃ§ Ã§arpÄ±m??? (inner product)
    




    32



Ben her sayÄ± dizisini tek tek oluÅŸturmayacaÄŸÄ±m. Genelde kullandÄ±ÄŸÄ±m dizilerin
bir dÃ¼zeni olacak. Bunlar iÃ§in hazÄ±r fonksiyonlar yok mu?


    b = numpy.arange(0,10,2) #sÄ±ralÄ± dizi Ã¼retme. baÅŸlangÄ±Ã§,bitiÅŸ(diziye dahil deÄŸil), aralÄ±k
    b




    array([0, 2, 4, 6, 8])




    b = numpy.arange(0,10,2)

Tamam. YalnÄ±z biz her iÅŸlem iÃ§in "numpy." ÅŸeklinde uzun uzun yazmasak


    from numpy import all    # Bu tavsiye edilmez
    b = eye(4)               # Birim matris. numpy.eye() aslÄ±nda
    b




    array([[ 1.,  0.,  0.,  0.],
           [ 0.,  1.,  0.,  0.],
           [ 0.,  0.,  1.,  0.],
           [ 0.,  0.,  0.,  1.]])



(*Bu yÃ¶ntem Ã§ok uygun deÄŸil. Ä°sim uzayÄ±mÄ±n (Namespace: ) Ã§orbaya dÃ¶nmesine neden
oluyor. Ã–rneÄŸin birÃ§ok modÃ¼l altÄ±nda aynÄ± isimli fonksiyon ve deÄŸiÅŸken olabilir
(Ã¶r: math.sin(), numpy.sin). Hepsini aynÄ± isimuzayÄ±na attÄ±ÄŸÄ±mda birbirlerini
gÃ¶lgeleyeceklerdir (sadece bir sin() fonksiyonu bu isimle Ã§aÄŸrÄ±labilecek).
ModÃ¼lismi.fonksiyon() tarzÄ±nda kullandÄ±ÄŸÄ±mda bu karmaÅŸÄ±klÄ±ÄŸÄ± Ã¶nleyebilirim.* )
<br>
Peki ne Ã¶nerirsin?


    import numpy as np #Takma ad (alias) ile kÄ±saltma


    c = np.random.randn(3,3) # HiyerarÅŸiye dikkat! Numpy(np) altÄ±ndaki random altÄ±ndaki randn fonksiyonu 
    c                        # randn normal (gauss) daÄŸÄ±lÄ±mÄ±nda rastgele sayÄ±lar Ã¼retir




    array([[ 1.29844181, -0.02076778,  1.27033544],
           [ 0.07086581, -0.12473456,  0.4437992 ],
           [ 0.59667001, -0.26232953, -0.38660665]])



Bu yÃ¶ntem iyiymiÅŸ. Ama diyelimki numpy.random altÄ±ndaki fonksiyonlarÄ± Ã§ok sÄ±k
kullanÄ±yorum. AynÄ± yÃ¶ntemi yine kullanabilir miyim?


    import numpy.random as npr


    c = npr.rand(2,3) # numpy.random.rand(). Bu fonksiyon birÃ¶rnek (uniform) daÄŸÄ±lÄ±mda rastgele sayÄ±lar Ã¼retir 
    c




    array([[ 0.94670994,  0.26017765,  0.73622775],
           [ 0.42069041,  0.15319554,  0.74341128]])



Bir gÃ¼zellik daha


    import numpy as np
    a = np.array([[1./6., 1./4.], [1./3., 1./2.]]) * np.pi # radyan cinsinden [[30, 45], [60, 90]] derece 
    a




    array([[ 0.52359878,  0.78539816],
           [ 1.04719755,  1.57079633]])




    b = np.sin(a) # fonksiyon tÃ¼m elemanlara uygulanÄ±r
    b




    array([[ 0.5       ,  0.70710678],
           [ 0.8660254 ,  1.        ]])




    a = np.array([[1, 2], [3, 4]])
    b = np.array([[5, 6]])
    np.concatenate((a, b), axis=0)




    array([[1, 2],
           [3, 4],
           [5, 6]])



## Muhabbet renkleniyor

SayÄ±larla oynamak gÃ¼zel. Birde bunlarÄ± bir grafikte gÃ¶rsek.


    import matplotlib.pyplot as plt # yine birÅŸeyler geliyor


    x = np.arange(0,11)
    y = x**2
    plt.plot(x,y)
    plt.show()


![png](AB15_Python_Bilimsel_Hesaplama_files/AB15_Python_Bilimsel_Hesaplama_109_0.png)


Bu grafiÄŸi biraz ÅŸenlendirsek ama


    plt.title("Biraz Senlendirilmis Matplotlib")
    plt.xlabel("x ekseni")
    plt.ylabel("y ekseni")
    plt.grid(True)
    plt.plot(x, y, 'g--')
    plt.bar(x, y)
    plt.annotate("$y = x^2$ grafigi", xy=(3, 60), color = 'r')
    plt.show()


![png](AB15_Python_Bilimsel_Hesaplama_files/AB15_Python_Bilimsel_Hesaplama_111_0.png)



    

YardÄ±m

Boolean values and comparison operators

Strings

Lists

Tuples and immutable versus mutable objects

Assignment and name binding


    

If statements

For loops

List comprehensions

While loops

Functions

Function namespaces

Writing scripts

Modules


    

Timing functions and programs


    import time
    time.time() 
    




    1424019262.912




    t1 = time.time() 
    ComputeEnergies() 
    t2 = time.time()


    ---------------------------------------------------------------------------
    NameError                                 Traceback (most recent call last)

    <ipython-input-62-2ea4b62b6b55> in <module>()
          1 t1 = time.time()
    ----> 2 ComputeEnergies()
          3 t2 = time.time()
    

    NameError: name 'ComputeEnergies' is not defined



    import cProfile
    cProfile.run("ComputeEnergies()")

             2 function calls in 0.000 seconds
    
       Ordered by: standard name
    
       ncalls  tottime  percall  cumtime  percall filename:lineno(function)
            1    0.000    0.000    0.000    0.000 <string>:1(<module>)
            1    0.000    0.000    0.000    0.000 {method 'disable' of '_lsprof.Profiler' objects}
    
    
    


    ---------------------------------------------------------------------------
    NameError                                 Traceback (most recent call last)

    <ipython-input-63-ddca58c435a1> in <module>()
          1 import cProfile
    ----> 2 cProfile.run("ComputeEnergies()")
    

    C:\Python27\lib\cProfile.pyc in run(statement, filename, sort)
         27     try:
         28         try:
    ---> 29             prof = prof.run(statement)
         30         except SystemExit:
         31             pass
    

    C:\Python27\lib\cProfile.pyc in run(self, cmd)
        133         import __main__
        134         dict = __main__.__dict__
    --> 135         return self.runctx(cmd, dict, dict)
        136 
        137     def runctx(self, cmd, globals, locals):
    

    C:\Python27\lib\cProfile.pyc in runctx(self, cmd, globals, locals)
        138         self.enable()
        139         try:
    --> 140             exec cmd in globals, locals
        141         finally:
        142             self.disable()
    

    <string> in <module>()
    

    NameError: name 'ComputeEnergies' is not defined



    


    

# Python Nesne YÃ¶nelimli Programlama

Python Python enforces a great democracy: everything in itâ€”values, lists,
classes, and functionsâ€”are objects.
An object comes with multiple properties and functions that can accessed using
dot notation.
For example,


    s = "hello" 
    s.capitalize() 
    s.replace("lo", "p") 




    'help'



We could have used dot notation directly on the string itself:


    "hello".capitalize() 




    'Hello'



The fact that everything is an object has great advantages for programming
flexibility.
Any object can be passed to a function; one can send values or arrays, for
example,
but it is equally easy to send other functions as arguments to functions.
Moreover, almost everything in Python can be packaged up and saved to a file,
since there are generic routines that pack and unpack objects into strings.

# python-control-flow

A simple while loop -- notice the indentation to denote the block that is part
of the loop.


    n = 0
    while n < 10:
        print n
        n += 1
    

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    

if allows for branching.  python does not have a select/case statement


    x = 10
    if x < 0:
        print "negative"
    elif x == 0:
        print "zero"
    else:
        print "positive"
    

    positive
    

it's easy to loop over items in a list


    alist = [1, 2.0, "three", 4]
    for a in alist:
        print a
    

    1
    2.0
    three
    4
    

and break out of the loop when you find what you're looking for


    n = 0
    for a in alist:
        if a == "three":
            break
        else:
            n += 1
    
    print n
    

    2
    

(for that example, however, there is a simpler way)


    print alist.index("three")

    2
    

for dictionaries, you can also loop over the elements


    myDict = {"key1":1, "key2":2, "key3":3}
    
    for k, v in myDict.iteritems():
        print "key = %s, value = %s" % (`k`, `v`)    # notice how we do the formatting here
    

    key = 'key3', value = 3
    key = 'key2', value = 2
    key = 'key1', value = 1
    


    


    Pitonlar pandalar ne oluyor 


      File "<ipython-input-72-0e87ba3fb057>", line 1
        Pitonlar pandalar ne oluyor
                        ^
    SyntaxError: invalid syntax
    


###### *Python' la muhabbetiniz bol olsun. YalnÄ±z bu iliÅŸki tek taraflÄ± olmaz.
UnutmayÄ±n kaynak sizsiniz!.* ######


    
