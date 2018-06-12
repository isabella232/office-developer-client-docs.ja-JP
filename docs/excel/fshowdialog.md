---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- fshowdialog function [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798889"
---
# <a name="fshowdialog"></a><span data-ttu-id="a1811-104">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="a1811-104">fShowDialog</span></span>

 <span data-ttu-id="a1811-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a1811-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a1811-p101">ネイティブ Windows ダイアログ ボックスの例を読み込んで表示するユーザー定義コマンドの例です。GENERIC.xll が読み込まれるとき、このコマンドにアクセスするユーザー定義メニュー [Generic] を作成します。</span><span class="sxs-lookup"><span data-stu-id="a1811-p101">Example user-defined command that loads and displays an example native Windows dialog box. When GENERIC.xll is loaded, it creates a user-defined menu, Generic, through which this command is accessed.</span></span>
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a><span data-ttu-id="a1811-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="a1811-108">Parameters</span></span>

<span data-ttu-id="a1811-109">���̊֐��ɂ̓p�����[�^�[�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="a1811-109">The function takes no parameters.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="a1811-110">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="a1811-110">Property value/Return value</span></span>

<span data-ttu-id="a1811-111">���̊֐��́A����Ɋ����������Ƃ���������l 0 ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="a1811-111">The function return integer zero to indicate successful completion</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a1811-112">����</span><span class="sxs-lookup"><span data-stu-id="a1811-112">Remarks</span></span>

<span data-ttu-id="a1811-113">�l�C�e�B�u Windows �_�C�A���O �{�b�N�X��\������菇�͎��̂Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="a1811-113">The steps to display the native Windows dialog box are as follows:</span></span>
  
1. <span data-ttu-id="a1811-114">**GetHwnd** ��g�p���āAMicrosoft Excel ���C�� �E�B���h�E �n���h����擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="a1811-114">Obtain the Microsoft Excel main Windows handle using **GetHwnd**.</span></span>
    
2. <span data-ttu-id="a1811-115">**HookExcelWindow** ��g�p���� Excel ���C�� �E�B���h�E��t�b�N���܂��B</span><span class="sxs-lookup"><span data-stu-id="a1811-115">Hook the Excel main window using **HookExcelWindow**.</span></span>
    
3. <span data-ttu-id="a1811-116">**DialogBox** �ɂ���ă_�C�A���O �{�b�N�X��\�����܂��B</span><span class="sxs-lookup"><span data-stu-id="a1811-116">Display the dialog box using **DialogBox**.</span></span>
    
4. <span data-ttu-id="a1811-117">**UnhookExcelWindow** ��g�p���� Excel ���C�� �E�B���h�E�̃t�b�N�������܂��B</span><span class="sxs-lookup"><span data-stu-id="a1811-117">Unhook the Excel main window using **UnhookExcelWindow**.</span></span>
    
### <a name="example"></a><span data-ttu-id="a1811-118">��</span><span class="sxs-lookup"><span data-stu-id="a1811-118">Example</span></span>

<span data-ttu-id="a1811-119">���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="a1811-119">See  `\SAMPLES\GENERIC\GENERIC.C` for the source code for this function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a1811-120">�֘A����</span><span class="sxs-lookup"><span data-stu-id="a1811-120">See also</span></span>



[<span data-ttu-id="a1811-121">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="a1811-121">Functions in the Generic DLL</span></span>](functions-in-the-generic-dll.md)

