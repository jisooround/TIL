# git branch
git branch란 특정한 시점에서 독립적으로 코드를 변경할 수 있도록 하는 모델입니다.
즉, 그 시점으로 부터 동일하게 복사한 평행 우주 공간이라고 생각하면 편합니다. 작업한 브랜치 내용에 문제가 없다면 메인 브랜치에 병합(Merge)해주어 변경사항을 적용할 수 있습니다. 이로써 독립된 브랜치를 활용하여 작업 단위로 버전관리를 할 수 있고, 실험적인 개발을 할 때에도 안전한 개발이 가능합니다.

## git branch command
`$ git branch` 현재 브랜치 확인하기
`$ git branch -r` remote상의 브랜치 확인하기 
`$ git branch setup` 'setup'이라는 브랜치 생성하기
`$ git switch setup` 'setup`이라는 브랜치로 이동하기
`$ git merge setup` 'setup'이라는 브랜치를 끌어와 병합하기
`$ git branch -D setup` 'setup'이라는 브랜치 삭제하기
`$ git branch -M newname` 브랜치 이름 바꾸기

## Merge
브랜치를 병합할 때에는 현재 브랜치를 'main'으로 하고, merge할 브랜치를 끌어오면 됩니다.
`$ git merge setup`'setup'이라는 브랜치를 병합한다는 의미입니다.
