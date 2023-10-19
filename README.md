# typescript-handbook

<h2>tsconfig.json</h2>
ex)
{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "strict": true,
    "esModuleInterop": true,
    "outDir": "./dist"
  }
}

target: 컴파일된 코드가 어떤 환경에서 실행될 지 정의
module: 컴파일된 코드가 어떤 모듈 시스템을 사용할 지 정의
strict: 모든 타입 체킹 옵션 활성화/비활성화
esModuleInterop: commonjs 모듈 형태로 이루어진 파일을 es2015 모듈 형태로 불러올 수 있게 함
outDir: 컴파일된 파일들이 저장되는 경로 지정

기본타입

불리언 (Boolean)
let isDone: boolean = false;

숫자 (Number)
let decimal: number = 6;

문자열 (String)
let color: string = "blue";

배열 (Array)
let list: number[] = [1, 2, 3];
let list: Array<number> = [1, 2, 3];

튜플 (Tuple)
x = ["hello", 10];

열거 (Enum)
enum Color {Red, Green, Blue}
let c: Color = Color.Green;

Any
let notSure: any = 4;

Void
function warnUser(): void {
    console.log("This is my warning message");
}

Null and Undefined
let u: undefined = undefined;
let n: null = null;

Never
function error(message: string): never {
    throw new Error(message);
}

객체 (Object)
declare function create(o: object | null): void;

타입 단언 (Type assertions)
let someValue: any = "this is a string";

let strLength: number = (<string>someValue).length;

let someValue: any = "this is a string";

let strLength: number = (someValue as string).length;

레퍼런스: https://typescript-kr.github.io/pages/basic-types.html
