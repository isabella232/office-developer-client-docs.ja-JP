---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- debugprintf function [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798769"
---
# <a name="debugprintf"></a><span data-ttu-id="66d0d-104">debugPrintf</span><span class="sxs-lookup"><span data-stu-id="66d0d-104">debugPrintf</span></span>

<span data-ttu-id="66d0d-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="66d0d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="66d0d-p101">Windows SDK �֐� **OutputDebugStringA** ��g�p���āA�A�N�e�B�u�ȃf�o�b�K�[�Ƀk���I�[������̏������݂�s���t���[�����[�N ���C�u�����֐��B�A�v���P�[�V�����Ƀf�o�b�K�[���Ȃ��ꍇ�́A�V�X�e���̃f�o�b�K�[�ɕ����񂪕\������܂��B�A�v���P�[�V�����Ƀf�o�b�K�[���Ȃ��A�V�X�e���̃f�o�b�K�[���A�N�e�B�u�łȂ��ꍇ�́A **debugPrintf** �͉��̓����s���܂���B</span><span class="sxs-lookup"><span data-stu-id="66d0d-p101">Framework library function that writes a null-terminated byte-string to the active debugger via the Windows SDK function **OutputDebugStringA**. If the application has no debugger, the system debugger displays the string. If the application has no debugger and the system debugger is not active, **debugPrintf** does nothing.</span></span> 
  
<span data-ttu-id="66d0d-109">���̊֐��͒l��Ԃ��܂���B</span><span class="sxs-lookup"><span data-stu-id="66d0d-109">This function does not return a value.</span></span>
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a><span data-ttu-id="66d0d-110">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="66d0d-110">Parameters</span></span>

 <span data-ttu-id="66d0d-111">_lpFormat (LPSTR)_</span><span class="sxs-lookup"><span data-stu-id="66d0d-111">_lpFormat (LPSTR)_</span></span>
  
<span data-ttu-id="66d0d-112">�\`��������ŁA **sprintf** �֐��ƂƂ�ɗp�����镶����̍\���ƃ��[���ɏ]���B</span><span class="sxs-lookup"><span data-stu-id="66d0d-112">The format string, which follows the syntax and rules for that used with the **sprintf** function.</span></span> 
  
 <span data-ttu-id="66d0d-113">_arguments_</span><span class="sxs-lookup"><span data-stu-id="66d0d-113">_arguments_</span></span>
  
<span data-ttu-id="66d0d-114">�\`��������Ɉ�v���� 0 �ȏ�̈����B</span><span class="sxs-lookup"><span data-stu-id="66d0d-114">Zero or more arguments to match the format string.</span></span>
  
## <a name="example"></a><span data-ttu-id="66d0d-115">��</span><span class="sxs-lookup"><span data-stu-id="66d0d-115">Example</span></span>

<span data-ttu-id="66d0d-p102">この関数は、関数にコントロールが渡されたことを示す文字列を印刷します。コンパイルする前に _DEBUG フラグを定義する必要があります。未定義のままでは、この関数は何の動作も行いません。</span><span class="sxs-lookup"><span data-stu-id="66d0d-p102">This function prints a string to show that control was passed to it. The _DEBUG flag must be defined before compiling or else this function does nothing.</span></span>
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a><span data-ttu-id="66d0d-118">�֘A����</span><span class="sxs-lookup"><span data-stu-id="66d0d-118">See also</span></span>



<span data-ttu-id="66d0d-119">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="66d0d-119">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

