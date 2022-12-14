# git branch
git branch란 특정한 시점에서 독립적으로 코드를 변경할 수 있도록 하는 모델입니다.
즉, 그 시점으로 부터 동일하게 복사한 평행 우주 공간이라고 생각하면 편합니다. 작업한 브랜치 내용에 문제가 없다면 메인 브랜치에 병합(Merge)해주어 변경사항을 적용할 수 있습니다. 이로써 독립된 브랜치를 활용하여 작업 단위로 버전관리를 할 수 있고, 실험적인 개발을 할 때에도 안전한 개발이 가능합니다.

## git branch command
`$ git branch` 현재 브랜치 확인하기<br>
`$ git branch -r` remote상의 브랜치 확인하기<br> 
`$ git branch setup` 'setup'이라는 브랜치 생성하기<br>
`$ git switch setup` 'setup'이라는 브랜치로 이동하기<br>
`$ git merge setup` 'setup'이라는 브랜치를 끌어와 병합하기<br>
`$ git branch -D setup` 'setup'이라는 브랜치 삭제하기<br>
`$ git branch -M newname` 브랜치 이름 바꾸기<br>

## Merge
브랜치를 병합할 때에는 현재 브랜치를 'main'으로 하고, merge할 브랜치를 끌어오면 됩니다.
`$ git merge setup`'setup'이라는 브랜치를 병합한다는 의미입니다.

## git confilct
git confilct이란 git merge로 인해 합쳐지면서 생기는 충돌을 의미합니다.
git 충돌시에 할 수 있는 선택은 두가지입니다.
1. 겹치는 두 내용을 재조합합니다.
2. 둘 내용 중 하나를 선택합니다.

## Trailing Comma
git은 라인 단위로 추적을 하기 때문에 줄바꿈 하는 것 자체를 변화로 인식하고, git 병합시에 연속성이 틀어질 우려가 있습니다. 이를 해결하기 위해서 요소 나열할 때 모두 줄바꿈을하고 마지막에 콤마를 붙이는 습관을 들여야합니다.

