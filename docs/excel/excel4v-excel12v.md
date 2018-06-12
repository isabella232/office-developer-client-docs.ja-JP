---
title: Excel4v/Excel12v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12v
- Excel4v
keywords:
- excel12v function [excel 2007],Excel4v function [Excel 2007]
localization_priority: Normal
ms.assetid: e3e96b98-c5a7-4625-95b6-a1e2d09c6d3d
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 7ffa0bc3ae6222af1ecd7f65de66d026ea178c87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798882"
---
# <a name="excel4vexcel12v"></a><span data-ttu-id="17844-104">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="17844-104">Excel4v/Excel12v</span></span>

 <span data-ttu-id="17844-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="17844-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="17844-106">Microsoft Excel ���[�N�V�[�g�̓���֐��A�}�N�� �V�[�g�֐���R�}���h�A�܂��� XLL �ŗL�̓���֐���R�}���h�� DLL�AXLL�A�܂��̓R�[�h ���\�[�X�������Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="17844-106">Calls an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command, from within a DLL, XLL, or code resource.</span></span>
  
<span data-ttu-id="17844-p101">Excel �̂��ׂĂ̍ŐV�o�[�W�����́A **Excel4v** ��T�|�[�g���Ă��܂��BExcel 2007 �ȍ~�̃o�[�W�����ł́A **Excel12v** ���T�|�[�g����Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="17844-p101">All recent versions of Excel support **Excel4v**. Starting in Excel 2007, **Excel12v** is supported.</span></span> 
  
<span data-ttu-id="17844-109">Excel には、DLL や XLL にコントロールが渡された場合にのみ、これらの関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="17844-109">These functions can be called only when Excel has passed control to the DLL or XLL.</span></span> <span data-ttu-id="17844-110">呼び出せるように Excel が経過するとしないコントロール直接に Visual Basic for Applications (VBA)。</span><span class="sxs-lookup"><span data-stu-id="17844-110">They can also be called when Excel has passed control indirectly via a call to Visual Basic for Applications (VBA).</span></span> <span data-ttu-id="17844-111">他の任意の時点で呼び出すことができません。</span><span class="sxs-lookup"><span data-stu-id="17844-111">They cannot be called at any other time.</span></span> <span data-ttu-id="17844-112">たとえば、DllMain 関数またはその他のオペレーティング システムには、DLL が呼び出されたときに、または DLL によって作成されたスレッドからの呼び出し時に呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="17844-112">For example, they cannot be called during calls to the DllMain function or other times when the operating system has called the DLL, or from a thread created by the DLL.</span></span> 
  
<span data-ttu-id="17844-p103">[Excel4 �� Excel12](excel4-excel12.md) �֐��́A�����̈�����X�^�b�N��̉ϒ����X�g�Ƃ��Ď󂯓���܂��B��� **Excel4v** ����� **Excel12v** �֐��́A�����̈�����z��Ƃ��Ď󂯓���܂��B����ȊO�̂�����_�ɂ����āA **Excel4** �� **Excel4v** �Ɠ����悤�ɓ��삵�A **Excel12** �� **Excel12v** �Ɠ����悤�ɓ��삵�܂��B</span><span class="sxs-lookup"><span data-stu-id="17844-p103">The [Excel4 and Excel12](excel4-excel12.md) functions accept their arguments as a variable length list on the stack, whereas the **Excel4v** and **Excel12v** functions accept their arguments as an array. In all other respects, **Excel4** behaves the same as **Excel4v**, and **Excel12** behaves the same as **Excel12v**.</span></span>
  
```cs
int _cdecl Excel4v(int iFunction, LPXLOPER pxRes, int iCount, LPXLOPER rgx[]);
int _cdecl Excel12v(int iFunction, LPXLOPER12 pxRes, int iCount, LPXLOPER12 rgx[]);
```

## <a name="parameters"></a><span data-ttu-id="17844-115">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="17844-115">Parameters</span></span>

 <span data-ttu-id="17844-116">_iFunction_(**int**)</span><span class="sxs-lookup"><span data-stu-id="17844-116">_iFunction_ (**int**)</span></span>
  
<span data-ttu-id="17844-p104">�Ăяo���R�}���h�A�֐��A�܂��͓���֐���������l�B _iFunction_ �̗L���Ȓl�̈ꗗ�́A���̉���Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="17844-p104">A number that indicates the command, function, or special function you want to call. For a list of valid  _iFunction_ values, see the following Remarks section.</span></span> 
  
 <span data-ttu-id="17844-119">_pxRes_(**LPXLOPER**または**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="17844-119">_pxRes_ (**LPXLOPER** or **LPXLOPER12**)</span></span>
  
<span data-ttu-id="17844-120">�]�����ꂽ�֐��̌��ʂ�ێ�����A **XLOPER** ( **Excel4v** �̏ꍇ) �܂��� **XLOPER12** ( **Excel12v** �̏ꍇ) �ւ̃|�C���^�[�B</span><span class="sxs-lookup"><span data-stu-id="17844-120">A pointer to an **XLOPER** (in the case of **Excel4v**) or an **XLOPER12** (in the case of **Excel12v**) that will hold the result of the evaluated function.</span></span>
  
 <span data-ttu-id="17844-121">_iCount_(**int**)</span><span class="sxs-lookup"><span data-stu-id="17844-121">_iCount_ (**int**)</span></span>
  
<span data-ttu-id="17844-p105">�֐��֓n������A�̈����̐��BExcel 2003 �܂ł̃o�[�W�����ł́A0 - 30 �̔C�ӂ̐��ł��BExcel 2007 �ȍ~�́A0 - 255 �̔C�ӂ̐��ł��B</span><span class="sxs-lookup"><span data-stu-id="17844-p105">The number of subsequent arguments that will be passed to the function. In versions of Excel up to 2003 this can be any number from 0 through 30. Starting in Excel 2007, this can be any number from 0 through 255.</span></span>
  
 <span data-ttu-id="17844-125">_rgx_(**LPXLOPER**または**LPXLOPER12**)</span><span class="sxs-lookup"><span data-stu-id="17844-125">_rgx_ (**LPXLOPER []** or **LPXLOPER12 []**)</span></span>
  
<span data-ttu-id="17844-p106">�֐��ւ̈�����܂ޔz��ł��B�z���̂��ׂĂ̈����� **XLOPER** �܂��� **XLOPER12** �̒l�ւ̃|�C���^�[�ł���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="17844-p106">An array that contains the arguments to the function. All arguments in the array must be pointers to **XLOPER** or **XLOPER12** values.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="17844-128">�߂�l</span><span class="sxs-lookup"><span data-stu-id="17844-128">Return value</span></span>

<span data-ttu-id="17844-129">�����̊֐��́A **Excel4** ����� **Excel12** �Ɠ����l��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="17844-129">These functions return the same values as **Excel4** and **Excel12**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17844-130">����</span><span class="sxs-lookup"><span data-stu-id="17844-130">Remarks</span></span>

<span data-ttu-id="17844-p107">�����̊֐��́A���Z�q�ɓn���ꂽ�����̐����ς̏ꍇ�ɖ𗧂��܂��B���Ƃ��� **Excel4v** ����� **Excel12v** �́A�����̍��v�����o�^�����֐����������̐��ɂ���Č��܂� [xlfRegister](xlfregister-form-1.md) ��g�p���Ċ֐���o�^����Ƃ��ɖ�ɗ����܂��B **Excel4** �܂��� **Excel12** �̃��b�p�[�֐���L�q����Ƃ��ɂ́A **Excel4v** ����� **Excel12v** ��֗��ł��B�����̏ꍇ�A�ό������X�g��σT�C�Y�̒P��̔z��̈����ɕϊ��� ( **Excel4** �܂��� **Excel12** �֒ʏ�ǂ���񋟂����悤��)�A **Excel4v** �܂��� **Excel12v** ��g�p���� Excel �ɃR�[���o�b�N����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="17844-p107">These functions are useful where the number of arguments passed to the operator is variable. For example, **Excel4v** and **Excel12v** are useful when you register functions by using [xlfRegister](xlfregister-form-1.md) where the number of total arguments depends on the number of arguments taken by the function being registered. **Excel4v** and **Excel12v** are also useful when you write a wrapper function for **Excel4** or **Excel12**. In these cases, you need to convert a variable argument list, as would normally be supplied to **Excel4** or **Excel12**, to a single array argument of variable size to call back into Excel by using **Excel4v** or **Excel12v**.</span></span>
  
### <a name="example"></a><span data-ttu-id="17844-135">��</span><span class="sxs-lookup"><span data-stu-id="17844-135">Example</span></span>

<span data-ttu-id="17844-136">�R�[�h�̗�ɂ��ẮA���Ɏ��� SDK ��C���X�g�[�������ꏊ�ɂ���AExcel 2010 XLL SDK �� **Excel** ����� **Excel12f** �֐��̃R�[�h��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="17844-136">For code examples, see the code for the **Excel** and **Excel12f** functions in the Excel 2010 XLL SDK, at the following location where you installed the SDK:</span></span> 
  
<span data-ttu-id="17844-137">Samples\Framewrk\Framewrk.c</span><span class="sxs-lookup"><span data-stu-id="17844-137">Samples\Framewrk\Framewrk.c</span></span>
  
## <a name="see-also"></a><span data-ttu-id="17844-138">�֘A����</span><span class="sxs-lookup"><span data-stu-id="17844-138">See also</span></span>



[<span data-ttu-id="17844-139">Excel4�AExcel12</span><span class="sxs-lookup"><span data-stu-id="17844-139">Excel4/Excel12</span></span>](excel4-excel12.md)

