---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798994"
---
# <a name="xlgetinstptr"></a><span data-ttu-id="9160b-103">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="9160b-103">xlGetInstPtr</span></span>

<span data-ttu-id="9160b-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9160b-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9160b-105">���� DLL ��Ăяo���Ă��� Microsoft Excel �C���X�^���X�̃C���X�^���X �n���h����Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="9160b-105">Returns the instance handle of the instance of Microsoft Excel that is currently calling a DLL.</span></span>
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a><span data-ttu-id="9160b-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="9160b-106">Parameters</span></span>

<span data-ttu-id="9160b-107">���̊֐��ɂ͈����͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="9160b-107">This function has no arguments.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="9160b-108">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="9160b-108">Property value/Return value</span></span>

<span data-ttu-id="9160b-109">インスタンス ハンドル (**xltypeBigData**) は、 **val.bigdata.h.hdata**フィールドになります。</span><span class="sxs-lookup"><span data-stu-id="9160b-109">The instance handle (**xltypeBigData**) will be in the **val.bigdata.h.hdata** field.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9160b-110">����</span><span class="sxs-lookup"><span data-stu-id="9160b-110">Remarks</span></span>

<span data-ttu-id="9160b-111">���̊֐���g�p����ƁADLL ��Ăяo���Ă��� Excel �̕����̎��s���C���X�^���X�����ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="9160b-111">This function can be used to distinguish between multiple running instances of Excel that are calling the DLL.</span></span>
  
<span data-ttu-id="9160b-112">この関数は、32 ビットと 64 ビットの両方のバージョンの Excel で適切な値を返します。</span><span class="sxs-lookup"><span data-stu-id="9160b-112">This function returns a correct value with both 32-bit and 64-bit versions of Excel.</span></span> <span data-ttu-id="9160b-113">導入 Excel 2010 の拡張機能として、 [xlGetInst](xlgetinst.md)関数を 32 ビット バージョンの Excel でのみ正常に動作します。</span><span class="sxs-lookup"><span data-stu-id="9160b-113">It was introduced in Excel 2010 as an extension to the [xlGetInst](xlgetinst.md) function, which works correctly only with 32-bit versions of Excel.</span></span> 
  
<span data-ttu-id="9160b-114">**XLOPER**および**XLOPER12**の両方は、 **xltypeBigData**の値をサポートしているのと同じ構造を持つための API のコールバック関数、 [Excel4 と Excel12](excel4-excel12.md)の種類を使用して呼び出されたときにこの関数が正常に動作します。入力します。</span><span class="sxs-lookup"><span data-stu-id="9160b-114">This function works correctly when it is called by using both the [Excel4 and Excel12](excel4-excel12.md) varieties of the API callback functions, because both **XLOPER** and **XLOPER12** have the same structure that supports the **xltypeBigData** value type.</span></span> 
  
## <a name="example"></a><span data-ttu-id="9160b-115">��</span><span class="sxs-lookup"><span data-stu-id="9160b-115">Example</span></span>

<span data-ttu-id="9160b-p102">���̎g�p��ł́A�Ō�ɌĂяo���� Excel �R�s�[ �C���X�^���X��A���݌Ăяo���Ă��� Excel �R�s�[�Ɣ�r���܂��B�����ꍇ�ɂ� 1 ��Ԃ��A�قȂ�ꍇ�ɂ� 0 ��Ԃ��܂��B�֐������s����ƁA-1 ��Ԃ��܂��B���̎g�p��́A32 �r�b�g�� 64 �r�b�g�̗����̃o�[�W������ Excel �ō쓮���܂��B</span><span class="sxs-lookup"><span data-stu-id="9160b-p102">The following example compares the instance of the last copy of Excel that called it to the current copy of Excel that called it. If they are the same, it returns 1; if not, it returns 0; if the function fails, it returns -1. This sample works with both 32-bit and 64-bit versions of Excel.</span></span>
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
    if (hNew != hOld)
    iRet = 0;
    else
    iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a><span data-ttu-id="9160b-119">�֘A����</span><span class="sxs-lookup"><span data-stu-id="9160b-119">See also</span></span>

- [<span data-ttu-id="9160b-120">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="9160b-120">xlGetHwnd</span></span>](xlgethwnd.md)
- [<span data-ttu-id="9160b-121">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="9160b-121">xlGetInst</span></span>](xlgetinst.md)
- [<span data-ttu-id="9160b-122">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="9160b-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

