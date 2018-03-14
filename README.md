# Laboratorijske vježbe za kolegij Strojno učenje (PMF Matematika) 2018

Laboratorijske vježbe za kolegij [Strojno učenje](https://web.math.pmf.unizg.hr/nastava/su/) na PMF Matematika u akademskoj godini 2017./2018. 

## Sadržaj vježbi

* [Vježba 1 - Priprema podataka i uvod u osnovne alate]()
* Vježba 2 - Nadzirano učenje
* Vježba 3 - Odabir značajki
* Vježba 4 - Smanjenje dimenzionalnosti
* Vježba 5 - Grupiranje 
* Vježba 6 - Duboko učenje

## Uputstva za instalaciju Anaconde

Vježbe se nalaze u formi Jupyter notebooks i testirane su na Windowsima, Linuxu i Mac OS X unutar [Anaconda](https://www.anaconda.com) (Python 3.6) environmenta (verzija 4.4.0). Za prvih pet vježbi vam neće trebati dodatni programski paketi pored onih koji dolaze s Anacondom. Za šestu vježbu (Duboko učenje) trebat će vam [TensorFlow](https://www.tensorflow.org) (verzija 1.3). Preporučamo da instalirate TensorFlow samo s CPU podrškom.

Slijedite uputstva u nastavku za vaš OS (Windows, Linux, Mac OS X):
* Downloadajte i instalirajte Anaconda-u s [https://www.anaconda.com/download/](https://www.anaconda.com/download/)
* Stvorite conda environment s Python 3.6 i standardnim Anaconda Python paketima (pogledajte [conda-cheatsheet](https://conda.io/docs/_downloads/conda-cheatsheet.pdf))
* Instalirajte TensorFlow 1.3 s CPU podrškom uz pomoć pip-a (uputstva na [https://www.tensorflow.org/install/](https://www.tensorflow.org/install/))

### Windows
TensorFlow instalacija je testirana na 64-bitnim Windows 7 i Windows 10, pošto trenutno nema podrške za TensorFlow na 32-bitnim sustavima. Preporučamo da instalirate TensorFlow u Anaconda environment. Downloadajte Anaconda (Python 3.6) za Windowse s [https://www.anaconda.com/download/](https://www.anaconda.com/download/) i instalirajte ih koristeći administratorske ovlasti.

Potom pokrenite Anaconda Command Prompt u administratorskom modu i
* Stvorite conda environment `vjezbe`:
  ```
  conda create --name vjezbe python=3.6 anaconda
  ```
* Akivirajte `vjezbe` s:
  ```
  activate vjezbe
  ```
* Instalirajte Tensorflow unutar `vjezbe`:
  ```
  pip install --ignore-installed --upgrade tensorflow
  ```

Za više informacija o tome kako instalirati TensorFlow na Windowsima pogledajte [https://www.tensorflow.org/install/install_windows](https://www.tensorflow.org/install/install_windows). Ako već imate stariju verziju Anaconda-e gdje Python 3.6 nije dostupan i dalje možete provesti navedenu proceduru, čime ćete instalirati Python 3.6 i učiniti ga dostupnim unutar `vjezbe` environment. Za više informacija oko rukovanja s Anaconda environmentima pogledajte [Managing environments](https://conda.io/docs/user-guide/tasks/manage-environments.html) u Anaconda dokumentaciji.

### Linux/Mac OS X
Slično kao i za Windowse, najjednostavniji način za instalaciju TensorFlowa na Linuxu ili Mac OS X je instalirati ga samo s CPU podrškom unutar Anaconda environment prema proceduri opisanoj ranije. Za detaljnija uputstva pogledajte:

* za Linux [https://www.tensorflow.org/install/install_linux#installing_with_anaconda](https://www.tensorflow.org/install/install_linux#installing_with_anaconda)

* za Mac OS X [https://www.tensorflow.org/install/install_mac#installing_with_anaconda](https://www.tensorflow.org/install/install_mac#installing_with_anaconda)

## Klonirajte Github repozitorij

Git je versioning program kojeg možete downloadati s [https://git-scm.com/downloads](https://git-scm.com/downloads). Iz komandne linije ([Anaconda] Command Prompt na Windowsima ili terminal na Linux/Mac OS X) pozicionirajte se u željeni direktorij i klonirajte git repozitorij s naredbom:
  ```
  git clone https://github.com/PMF-StrojnoUcenje2018/Vjezbe.git
  ```

Kao alternativnu možete jednostavno downloadati zip datoteku s [https://github.com/PMF-StrojnoUcenje2018/Vjezbe/archive/master.zip](https://github.com/PMF-StrojnoUcenje2018/Vjezbe/archive/master.zip), no ukoliko dođe do promjena u kodu morat ćete ponoviti cijeli postupak!

## Pokretanje Jupyter notebooks:
Sve vježbe su spremljene kao Jupyter notebooks [http://jupyter.org/] (Python bilježnice) koje možete pokrenuti na sljedeći način iz komadne linije:

* aktivirajte `vjezbe` conda environment (za više detalja pogledajte [conda-cheatsheet](https://conda.io/docs/_downloads/conda-cheatsheet.pdf)):

  - Windows: `activate vjezbe`

  - Linux/Mac OS X: `source activate vjezbe`

* unutar `vjezbe` pokrenite Jupyter Notebook server (za detalje pogledajte [uputstva](https://jupyter.readthedocs.io/en/latest/running.html#running)):
  ```
  jupyter notebook --notebook-dir=PATH-TO-REPOSITORY --port=NUMBER-OF-UNUSED-PORT
  ```
  Ovo će pokrenuti vaš pretpostavljeni web preglednik na `http://localhost:[NUMBER-OF-UNUSED-PORT]` nakon čega ćete moći navigirati strukturu direktorija i koristiti Jupyter notebooks za vježbe.