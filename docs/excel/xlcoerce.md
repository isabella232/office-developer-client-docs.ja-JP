---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- xlcoerce function [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798976"
---
# <a name="xlcoerce"></a><span data-ttu-id="43d5c-104">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="43d5c-104">xlCoerce</span></span>

 <span data-ttu-id="43d5c-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43d5c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="43d5c-106">**XLOPER**/ **XLOPER12** �̌^��ʂ̌^�ɕϊ����邩�A�V�[�g�̃Z���̒l��������܂��B</span><span class="sxs-lookup"><span data-stu-id="43d5c-106">Converts one type of **XLOPER**/ **XLOPER12** to another, or looks up cell values on a sheet.</span></span> 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a><span data-ttu-id="43d5c-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="43d5c-107">Parameters</span></span>

 <span data-ttu-id="43d5c-108">_pxSource_</span><span class="sxs-lookup"><span data-stu-id="43d5c-108">_pxSource_</span></span>
  
<span data-ttu-id="43d5c-109">�ϊ��Ώۂ̃\�[�X **XLOPER**/ **XLOPER12**�B</span><span class="sxs-lookup"><span data-stu-id="43d5c-109">The source **XLOPER**/ **XLOPER12** that needs to be converted.</span></span> 
  
 <span data-ttu-id="43d5c-110">_pxDestType_(**xltypeInt**)</span><span class="sxs-lookup"><span data-stu-id="43d5c-110">_pxDestType_ (**xltypeInt**)</span></span>
  
<span data-ttu-id="43d5c-111">(省略可能)。</span><span class="sxs-lookup"><span data-stu-id="43d5c-111">(Optional).</span></span> <span data-ttu-id="43d5c-112">結果の型のビット マスクを受け入れるように喜んでいます。</span><span class="sxs-lookup"><span data-stu-id="43d5c-112">A bit-mask of the resulting types you are willing to accept.</span></span> <span data-ttu-id="43d5c-113">複数の使用可能な型を指定するのには、ビットごとの**OR**演算子 (|) を使用してください。</span><span class="sxs-lookup"><span data-stu-id="43d5c-113">You should use the bitwise **OR** operator ( | ) to specify multiple possible types.</span></span> <span data-ttu-id="43d5c-114">この引数を省略すると、1 つのセルへの参照が値型の**xltypeStr**、 **xltypeNum**、 **xltypeBool**、 **xltypeErr**、 **xltypeNil** (参照先セルが空の場合)、およびブロックへの参照のいずれかに変換されます。セルは、 **xltypeMulti**に変換されます。</span><span class="sxs-lookup"><span data-stu-id="43d5c-114">If this argument is omitted, references to single cells are converted to one of the value types **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (if the referred-to cell is empty), and references to blocks of cells are converted to **xltypeMulti**.</span></span> <span data-ttu-id="43d5c-115">これにより、 **xlCoerce**はセルの値を検索する最も便利な方法です。</span><span class="sxs-lookup"><span data-stu-id="43d5c-115">This makes **xlCoerce** the most convenient way to look up cell values.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="43d5c-116">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="43d5c-116">Property value/Return value</span></span>

<span data-ttu-id="43d5c-117">(**XltypeStr**、 **xltypeNum**、 **xltypeBool**、 **xltypeErr**、 **xltypeNil**、または**xltypeMulti**) は、強制変換された値を返します。</span><span class="sxs-lookup"><span data-stu-id="43d5c-117">Returns the coerced value (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, or **xltypeMulti**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43d5c-118">����</span><span class="sxs-lookup"><span data-stu-id="43d5c-118">Remarks</span></span>

 <span data-ttu-id="43d5c-p102">**xlCoerce** �� **xltypeBigData** �܂��� **xltypeFlow** �ɕϊ��ł����A���̋t�̕ϊ���ł��܂���B **xltypeMissing** �܂��� **xltypeNil** �̌^��  _pxDestType_ �Ƃ��ēn�����Ƃ́A������ȗ����邱�Ƃɑ������܂��B�ꍇ�ɂ���ẮA�ϊ������s����ꍇ������܂��B���Ƃ��΁A������ɂ͐����ɕϊ��łȂ���̂�����܂��B</span><span class="sxs-lookup"><span data-stu-id="43d5c-p102">**xlCoerce** cannot convert to or from **xltypeBigData** or **xltypeFlow**. Passing an **xltypeMissing** or **xltypeNil** type as  _pxDestType_ is equivalent to omitting the argument. Conversion can fail in some cases. For example, some strings cannot be converted to numbers, whereas others can.</span></span> 
  
<span data-ttu-id="43d5c-123">�z��܂��͕����Z���̎Q�Ƃ�P��l�̌^�ɕϊ�����ƁA���ʂ͈�ԏ�̍��̃Z���܂��͔z��̗v�f�̒l�ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="43d5c-123">If an array or a multi-cell reference is converted to a single value type, the result is the value of the top left cell or array element.</span></span>
  
## <a name="example"></a><span data-ttu-id="43d5c-124">��</span><span class="sxs-lookup"><span data-stu-id="43d5c-124">Example</span></span>

<span data-ttu-id="43d5c-125">���̃R�[�h�́A `\SAMPLES\EXAMPLE\EXAMPLE.C` �ɂ���܂��B</span><span class="sxs-lookup"><span data-stu-id="43d5c-125">The following code can be found in  `\SAMPLES\EXAMPLE\EXAMPLE.C`.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="43d5c-p103">�����Ɏ�����鋭���菇���폜����A **xInt** ������ **xlcAlert** �ɓn�����悤�ɁA **xlcAlert** �֐��͈ÖٓI�Ɉ����𕶎���ɕϊ����悤�Ƃ��܂��B **xlcAlert** �̓R�}���h�̃}�N���ł��邽�߁A���̃R�[�h�̓}�N�� �V�[�g����Ăяo���ꂽ�Ƃ��̂ݐ������쓮���܂��B</span><span class="sxs-lookup"><span data-stu-id="43d5c-p103">The **xlcAlert** function implicitly tries to convert its argument to a string so that the coercion step shown here could in fact be removed, and **xInt** could be passed directly to **xlcAlert**. As **xlcAlert** is a command macro, this code only works correctly when called from a macro sheet.</span></span> 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="43d5c-128">�֘A����</span><span class="sxs-lookup"><span data-stu-id="43d5c-128">See also</span></span>



[<span data-ttu-id="43d5c-129">xlSet</span><span class="sxs-lookup"><span data-stu-id="43d5c-129">xlSet</span></span>](xlset.md)


[<span data-ttu-id="43d5c-130">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="43d5c-130">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

