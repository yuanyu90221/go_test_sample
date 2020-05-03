# go_test_sample

## go test 用法

1) 使用內建 testing package的用法

1 在要測試的對應檔案 寫一個對應的 ${filename}_test.go

2 在測試檔案 import testing這個內建test package

3 測試檔案:  func name必須為Test開頭,並且以 testing.T型別為輸入參數

func TestSample(t *testing.T) {

  // 測試內容

}

4 t.Fatal, t.Error用來印出測試結果

t.Fatal會直接中斷測試 印出結果

t.Error 會等到測試結束才印出結果

5 執行方式: go test -v ${testfile path}

## go test with testify

testify 測試小工具



github.com/stretchr/testify



裡面用 assert系列的工具可以用



測試指令

go test -v -run=${testfuncName} ./car

## 平行測試

## Bechmark Test

  go test -v --bench=. .

## run benchmark only and show memory

  go test -v --bench=. -run=none --benchmem .