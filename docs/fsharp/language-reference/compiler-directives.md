---
title: "컴파일러 지시문(F#)"
description: "F # 언어 전처리기 지시문, 조건부 컴파일 지시문, line 지시문과 컴파일러 지시문에 알아봅니다."
keywords: "visual f#, f#, 함수형 프로그래밍"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: 93aef07a-6747-4ce4-a10f-a05168978af6
ms.openlocfilehash: b4305d24163f9b23631d5efb6e838f55127cd9f5
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/18/2017
---
# <a name="compiler-directives"></a><span data-ttu-id="28ba7-104">컴파일러 지시문</span><span class="sxs-lookup"><span data-stu-id="28ba7-104">Compiler Directives</span></span>

<span data-ttu-id="28ba7-105">이 항목에서는 처리기 지시문과 컴파일러 지시문에 대해 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-105">This topic describes processor directives and compiler directives.</span></span>


## <a name="preprocessor-directives"></a><span data-ttu-id="28ba7-106">전처리기 지시문</span><span class="sxs-lookup"><span data-stu-id="28ba7-106">Preprocessor Directives</span></span>
<span data-ttu-id="28ba7-107">전처리기 지시문은 # 기호를 접두사로 사용하며 따로 한 줄을 할애하여 지시문을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-107">A preprocessor directive is prefixed with the # symbol and appears on a line by itself.</span></span> <span data-ttu-id="28ba7-108">이 지시문은 컴파일러 자체보다 먼저 실행되는 전처리기를 통해 해석됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-108">It is interpreted by the preprocessor, which runs before the compiler itself.</span></span>

<span data-ttu-id="28ba7-109">다음 표에는 F#에서 사용할 수 있는 전처리기 지시문의 목록이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-109">The following table lists the preprocessor directives that are available in F#.</span></span>


|<span data-ttu-id="28ba7-110">지시문</span><span class="sxs-lookup"><span data-stu-id="28ba7-110">Directive</span></span>|<span data-ttu-id="28ba7-111">설명</span><span class="sxs-lookup"><span data-stu-id="28ba7-111">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="28ba7-112">`#if`*기호*</span><span class="sxs-lookup"><span data-stu-id="28ba7-112">`#if` *symbol*</span></span>|<span data-ttu-id="28ba7-113">조건부 컴파일을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-113">Supports conditional compilation.</span></span> <span data-ttu-id="28ba7-114">다음 섹션의 코드는 `#if` 경우 포함 됩니다는 *기호* 정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-114">Code in the section after the `#if` is included if the *symbol* is defined.</span></span>|
|`#else`|<span data-ttu-id="28ba7-115">조건부 컴파일을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-115">Supports conditional compilation.</span></span> <span data-ttu-id="28ba7-116">위의 `#if`와 함께 사용되는 기호를 정의하지 않은 경우 포함할 코드 섹션을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-116">Marks a section of code to include if the symbol used with the previous `#if` is not defined.</span></span>|
|`#endif`|<span data-ttu-id="28ba7-117">조건부 컴파일을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-117">Supports conditional compilation.</span></span> <span data-ttu-id="28ba7-118">코드의 조건부 섹션이 끝나는 지점을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-118">Marks the end of a conditional section of code.</span></span>|
|<span data-ttu-id="28ba7-119">`#`[line] *int*,</span><span class="sxs-lookup"><span data-stu-id="28ba7-119">`#`[line] *int*,</span></span><br/><span data-ttu-id="28ba7-120">`#`[line] *int* *문자열*,</span><span class="sxs-lookup"><span data-stu-id="28ba7-120">`#`[line] *int* *string*,</span></span><br/><span data-ttu-id="28ba7-121">`#`[line] *int* *축 자 문자열*</span><span class="sxs-lookup"><span data-stu-id="28ba7-121">`#`[line] *int* *verbatim-string*</span></span>|<span data-ttu-id="28ba7-122">디버깅을 위해 원본 소스 코드 줄과 파일 이름을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-122">Indicates the original source code line and file name, for debugging.</span></span> <span data-ttu-id="28ba7-123">이 기능은 F# 소스 코드를 생성하는 도구에서 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-123">This feature is provided for tools that generate F# source code.</span></span>|
|<span data-ttu-id="28ba7-124">`#nowarn`*warningcode*</span><span class="sxs-lookup"><span data-stu-id="28ba7-124">`#nowarn` *warningcode*</span></span>|<span data-ttu-id="28ba7-125">컴파일러 경고를 해제합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-125">Disables a compiler warning or warnings.</span></span> <span data-ttu-id="28ba7-126">경고를 해제하려면 컴파일러 출력에서 해당 번호를 찾아 따옴표에 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-126">To disable a warning, find its number from the compiler output and include it in quotation marks.</span></span> <span data-ttu-id="28ba7-127">"FS" 접두사를 생략합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-127">Omit the "FS" prefix.</span></span> <span data-ttu-id="28ba7-128">같은 줄에서 여러 경고 번호를 해제하려면 각 번호를 따옴표에 포함하고 각 문자열을 공백으로 구분합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-128">To disable multiple warning numbers on the same line, include each number in quotation marks, and separate each string by a space.</span></span> <span data-ttu-id="28ba7-129">예:</span><span class="sxs-lookup"><span data-stu-id="28ba7-129">For example:</span></span>

`#nowarn "9" "40"`


<span data-ttu-id="28ba7-130">경고 해제 효과 지시문 앞에 있는 파일의 일부를 포함 하 여 전체 파일에 적용 됩니다. |</span><span class="sxs-lookup"><span data-stu-id="28ba7-130">The effect of disabling a warning applies to the entire file, including portions of the file that precede the directive.|</span></span>

## <a name="conditional-compilation-directives"></a><span data-ttu-id="28ba7-131">조건부 컴파일 지시문</span><span class="sxs-lookup"><span data-stu-id="28ba7-131">Conditional Compilation Directives</span></span>
<span data-ttu-id="28ba7-132">이러한 지시문 중 하나에 의해 비활성화 된 코드는 Visual studio 코드 편집기에서 흐리게 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-132">Code that is deactivated by one of these directives appears dimmed in the Visual StudioCode Editor.</span></span>


>[!NOTE] 
<span data-ttu-id="28ba7-133">다른 언어에 있는 그대로 동일한 조건부 컴파일 지시문의 동작을 볼 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-133">The behavior of the conditional compilation directives is not the same as it is in other languages.</span></span> <span data-ttu-id="28ba7-134">예를 들어 기호가 포함된 부울 식은 사용할 수 없으며 `true` 및 `false`가 특별한 의미를 가지지도 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-134">For example, you cannot use Boolean expressions involving symbols, and `true` and `false` have no special meaning.</span></span> <span data-ttu-id="28ba7-135">`if` 지시문에 사용하는 기호는 명령줄이나 프로젝트 설정에서 정의해야 합니다. `define` 전처리기 지시문이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-135">Symbols that you use in the `if` directive must be defined by the command line or in the project settings; there is no `define` preprocessor directive.</span></span>


<span data-ttu-id="28ba7-136">다음 코드에서는 `#if`, `#else` 및 `#endif` 지시문을 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-136">The following code illustrates the use of the `#if`, `#else`, and `#endif` directives.</span></span> <span data-ttu-id="28ba7-137">이 예제의 코드에는 `function1`에 대한 두 가지 버전의 정의가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-137">In this example, the code contains two versions of the definition of `function1`.</span></span> <span data-ttu-id="28ba7-138">때 `VERSION1` 사용 하 여 정의 [-define 컴파일러 옵션](https://msdn.microsoft.com/library/434394ae-0d4a-459c-a684-bffede519a04), 사이 코드는 `#if` 지시문 및 `#else` 지시문 활성화 됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-138">When `VERSION1` is defined by using the [-define compiler option](https://msdn.microsoft.com/library/434394ae-0d4a-459c-a684-bffede519a04), the code between the `#if` directive and the `#else` directive is activated.</span></span> <span data-ttu-id="28ba7-139">그렇지 않은 경우에는 `#else`와 `#endif` 사이의 코드가 활성화됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-139">Otherwise, the code between `#else` and `#endif` is activated.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7301.fs)]

<span data-ttu-id="28ba7-140">F#에는 `#define` 전처리기 지시문이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-140">There is no `#define` preprocessor directive in F#.</span></span> <span data-ttu-id="28ba7-141">`#if` 지시문에 사용되는 기호를 정의하려면 컴파일러 옵션이나 프로젝트 설정을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-141">You must use the compiler option or project settings to define the symbols used by the `#if` directive.</span></span>

<span data-ttu-id="28ba7-142">조건부 컴파일 지시문은 중첩하여 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-142">Conditional compilation directives can be nested.</span></span> <span data-ttu-id="28ba7-143">전처리기 지시문에서 들여쓰기는 중요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-143">Indentation is not significant for preprocessor directives.</span></span>


## <a name="line-directives"></a><span data-ttu-id="28ba7-144">줄 지시문</span><span class="sxs-lookup"><span data-stu-id="28ba7-144">Line Directives</span></span>
<span data-ttu-id="28ba7-145">빌드 과정에서 컴파일러를 통해 F# 코드의 오류를 보고할 때는 각 오류의 발생 지점에 해당하는 줄 번호가 참조 정보로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-145">When building, the compiler reports errors in F# code by referencing line numbers on which each error occurs.</span></span> <span data-ttu-id="28ba7-146">이러한 줄 번호는 1부터 시작합니다. 파일의 맨 첫 줄이 1번입니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-146">These line numbers start at 1 for the first line in a file.</span></span> <span data-ttu-id="28ba7-147">그러나 다른 도구를 사용하여 F# 소스 코드를 생성하는 경우에는 생성된 코드의 줄 번호가 일반적으로 크게 중요하지 않습니다. 생성된 F# 코드의 오류가 다른 소스에서 발생한 것일 가능성이 높기 때문입니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-147">However, if you are generating F# source code from another tool, the line numbers in the generated code are generally not of interest, because the errors in the generated F# code most likely arise from another source.</span></span> <span data-ttu-id="28ba7-148">`#line` 지시문을 사용하면 다른 도구를 통해 F# 소스 코드를 생성할 때 원래 줄 번호와 소스 파일에 대한 정보를 생성된 F# 코드에 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-148">The `#line` directive provides a way for authors of tools that generate F# source code to pass information about the original line numbers and source files to the generated F# code.</span></span>

<span data-ttu-id="28ba7-149">`#line` 지시문을 사용하는 경우 파일 이름을 따옴표로 묶어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-149">When you use the `#line` directive, file names must be enclosed in quotation marks.</span></span> <span data-ttu-id="28ba7-150">문자열 앞에 축자 토큰(`@`)이 오지 않는 경우 백슬래시 문자를 경로에 사용하려면 한 개가 아닌 두 개의 백슬래시 문자를 사용하여 이를 이스케이프해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-150">Unless the verbatim token (`@`) appears in front of the string, you must escape backslash characters by using two backslash characters instead of one in order to use them in the path.</span></span> <span data-ttu-id="28ba7-151">다음은 유효한 줄 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-151">The following are valid line tokens.</span></span> <span data-ttu-id="28ba7-152">이 예제에서는 도구를 사용하여 원래 파일 `Script1`을 실행한 결과로 F# 코드 파일이 자동 생성되며 이러한 지시문이 있는 위치의 코드가 파일 `Script1`의 25번 줄에 있는 몇몇 토큰으로부터 생성되는 것으로 가정합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-152">In these examples, assume that the original file `Script1` results in an automatically generated F# code file when it is run through a tool, and that the code at the location of these directives is generated from some tokens at line 25 in file `Script1`.</span></span>

[!code-fsharp[Main](../../../samples/snippets/fsharp/lang-ref-2/snippet7303.fs)]

<span data-ttu-id="28ba7-153">이 토큰은 해당 위치에서 생성되는 F# 코드가 `Script1`의 `25`번 줄 또는 그 부근에 있는 몇몇 구문으로부터 파생됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-153">These tokens indicate that the F# code generated at this location is derived from some constructs at or near line `25` in `Script1`.</span></span>


## <a name="compiler-directives"></a><span data-ttu-id="28ba7-154">컴파일러 지시문</span><span class="sxs-lookup"><span data-stu-id="28ba7-154">Compiler Directives</span></span>
<span data-ttu-id="28ba7-155">컴파일러 지시문은 # 기호가 접두사로 사용된다는 점에서 전처리기 지시문과 형태가 비슷하지만 전처리기에 의해 해석되지 않고 컴파일러를 통해 해석 및 처리되도록 남겨진다는 점에서 차이가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-155">Compiler directives resemble preprocessor directives, because they are prefixed with a # sign, but instead of being interpreted by the preprocessor, they are left for the compiler to interpret and act on.</span></span>

<span data-ttu-id="28ba7-156">다음 표에는 F#에서 사용할 수 있는 컴파일러 지시문이 나와 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-156">The following table lists the compiler directive that is available in F#.</span></span>


|<span data-ttu-id="28ba7-157">지시문</span><span class="sxs-lookup"><span data-stu-id="28ba7-157">Directive</span></span>|<span data-ttu-id="28ba7-158">설명</span><span class="sxs-lookup"><span data-stu-id="28ba7-158">Description</span></span>|
|---------|-----------|
|<span data-ttu-id="28ba7-159">`#light`["on"</span><span class="sxs-lookup"><span data-stu-id="28ba7-159">`#light` ["on"</span></span>|<span data-ttu-id="28ba7-160">"off"]</span><span class="sxs-lookup"><span data-stu-id="28ba7-160">"off"]</span></span>|<span data-ttu-id="28ba7-161">다른 ML 버전과의 호환성을 위해 간단한 구문을 사용하거나 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-161">Enables or disables lightweight syntax, for compatibility with other versions of ML.</span></span> <span data-ttu-id="28ba7-162">기본적으로 간단한 구문을 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-162">By default, lightweight syntax is enabled.</span></span> <span data-ttu-id="28ba7-163">자세한 구문은 항상 사용할 수 있도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-163">Verbose syntax is always enabled.</span></span> <span data-ttu-id="28ba7-164">따라서 간단한 구문과 자세한 구문을 함께 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-164">Therefore, you can use both lightweight syntax and verbose syntax.</span></span> <span data-ttu-id="28ba7-165">`#light` 지시문 자체는 `#light "on"`과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-165">The directive `#light` by itself is equivalent to `#light "on"`.</span></span> <span data-ttu-id="28ba7-166">`#light "off"`를 지정하는 경우에는 모든 언어 구문에 대해 자세한 구문 형식을 사용해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-166">If you specify `#light "off"`, you must use verbose syntax for all language constructs.</span></span> <span data-ttu-id="28ba7-167">F# 관련 설명에 나오는 구문은 간단한 구문을 사용하는 것을 전제로 하여 제시됩니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-167">Syntax in the documentation for F# is presented with the assumption that you are using lightweight syntax.</span></span> <span data-ttu-id="28ba7-168">자세한 내용은 참조 [자세한 구문](verbose-syntax.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-168">For more information, see [Verbose Syntax](verbose-syntax.md).</span></span>|
<span data-ttu-id="28ba7-169">해석기 (fsi.exe) 지시문에 대 한 참조 [F #을 사용한 대화형 프로그래밍](../tutorials/fsharp-interactive/index.md)합니다.</span><span class="sxs-lookup"><span data-stu-id="28ba7-169">For interpreter (fsi.exe) directives, see [Interactive Programming with F#](../tutorials/fsharp-interactive/index.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="28ba7-170">참고 항목</span><span class="sxs-lookup"><span data-stu-id="28ba7-170">See Also</span></span>
[<span data-ttu-id="28ba7-171">F# 언어 참조</span><span class="sxs-lookup"><span data-stu-id="28ba7-171">F# Language Reference</span></span>](index.md)

[<span data-ttu-id="28ba7-172">컴파일러 옵션</span><span class="sxs-lookup"><span data-stu-id="28ba7-172">Compiler Options</span></span>](compiler-options.md)
