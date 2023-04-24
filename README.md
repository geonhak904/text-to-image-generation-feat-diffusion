# text-to-image-generation

This is the repository of Pseudo Lab's Text-to-Image Generation (feat. Diffusion) team.

:bulb: Our aim is to review papers and code related to image generation and text-to-image generation models, approach them theoretically, and conduct various experiments by fine-tuning Diffusion based models.

[About Us - Pseudo Lab](https://www.linkedin.com/company/pseudolab/)

[About Us - Text-to-Image Generation (feat. Diffusion) Team](https://pseudo-lab.com/Text-to-Image-Generation-feat-Diffusion-cc12047d1bfc4bdfa70122c11ff90aee)

참여 방법: 매주 수요일 오후 9시, 가짜연구소 Discord Room-DH 로 입장!

## Contributor 
- 조상우 [Sangwoo Jo] | [Github](https://github.com/jasonjo97) | [Linkedin](https://www.linkedin.com/in/sangwoojo/) | 
- 문광수 [Kwangsu Mun] | | [Github](https://github.com/mksoo) | [Linkedin](https://www.linkedin.com/in/%EA%B4%91%EC%88%98-%EB%AC%B8-95681b229/) |
- 김지수 [Jisu Kim] | [Linkedin](https://www.linkedin.com/in/%EC%A7%80%EC%88%98-%EA%B9%80-5a0b2320a/) |
- 박범수 [Beomsoo Park] | [Github](https://github.com/hanlyang0522) |

## Schedule 
| idx | Date | Presenter | Paper / Code | 
| :--: | :--: | :--: | :--: |
| 1 | 2023.03.29 | 조상우 [Sangwoo Jo] | [Auto-Encoding Variational Bayes](https://arxiv.org/abs/1312.6114) (ICLR 2014) <br> [Generative Adversarial Networks](https://arxiv.org/abs/1406.2661) (NIPS 2014)| 
| 2 | 2023.04.05 | 문광수 [Kwangsu Mun] <br> 김지수 [Jisu Kim] | [Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks](https://arxiv.org/abs/1703.10593) (ICCV 2017) <br> [A Style-Based Generator Architecture for Generative Adversarial Networks](https://arxiv.org/abs/1406.2661) (CVPR 2019)| 

## Jupyter Book Update Procedure  
1. Clone the repo on your local computer  
```bash
git clone https://github.com/Pseudo-Lab/text-to-image-generation.git
```

2. Install required packages 
```bash
pip install jupyter-book==0.15.1
pip install ghp-import==2.1.0
```

3. Change the contents in ```book/docs``` folder with the following format and update ```_toc.yml``` file accordingly (check [https://github.com/Pseudo-Lab/SegCrew-Book](https://github.com/Pseudo-Lab/SegCrew-Book) for reference)

- 3.1. Add information section on top of the markdown page 
```{admonition} Information
- **Title:** {논문 제목}, {학회/학술지명}

- **Reference**
    - Paper:  [{논문 링크}]({논문 링크})
    - Code: [{code 링크}]({code 링크})
    - Review: [{review 링크}]({review 링크})
    
- **Author:** {리뷰 작성자 기입}

- **Edited by:** {리뷰 편집자 기입}

- **Last updated on {최종 update 날짜 e.g. Apr. 12, 2023}**
```

- 3-2. Use the following template when displaying images 
```
:::{figure-md} 'tag명'
<img src="{주소}" alt="{tag명}" class="bg-primary mb-1" width="{800px}">

{제목} \  (source: {출처})
:::
```

- 3-3. Update ```_toc.yml``` file accordingly
```
format: jb-book
root: intro
parts:
- caption: Paper/Code Review
  chapters:
  - file: docs/review/vae
  - file: docs/review/gan
```

4. Build the book using Jupyter Book command
```bash
jupyter-book build ./book
```

5. Sync your local and remote repositories
```bash
cd text-to-image-generation
git add .
git commit -m "adding my first book!"
git push
```

6. Publish your Jupyter Book with Github Pages
```
ghp-import -n -p -f book/_build/html -m "initial publishing"
```