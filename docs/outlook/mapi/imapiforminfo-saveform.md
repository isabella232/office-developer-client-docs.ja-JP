---
title: imapiforminfosaveform
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321715"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="e08e2-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="e08e2-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="e08e2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e08e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e08e2-105">構成ファイルに特定のフォームの説明を保存します。</span><span class="sxs-lookup"><span data-stu-id="e08e2-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="e08e2-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e08e2-106">Parameters</span></span>

 <span data-ttu-id="e08e2-107">_szfilename_</span><span class="sxs-lookup"><span data-stu-id="e08e2-107">_szFileName_</span></span>
  
> <span data-ttu-id="e08e2-108">順番フォームの説明メッセージファイルの名前を示す文字列。説明は保存されます。</span><span class="sxs-lookup"><span data-stu-id="e08e2-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="e08e2-109">このファイル名には、拡張子 fdm を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="e08e2-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e08e2-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="e08e2-110">Return value</span></span>

<span data-ttu-id="e08e2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e08e2-111">S_OK</span></span> 
  
> <span data-ttu-id="e08e2-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e08e2-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e08e2-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="e08e2-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="e08e2-114">構成ファイルを書き込めませんでした。</span><span class="sxs-lookup"><span data-stu-id="e08e2-114">The configuration file could not be written.</span></span> <span data-ttu-id="e08e2-115">エラーに関連付けられている[MAPIERROR](mapierror.md)構造体を取得するには、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e08e2-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="e08e2-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="e08e2-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="e08e2-117">**saveform**は、ローカルフォームコンテナーにフォームを保存するために呼び出された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e08e2-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="e08e2-118">**saveform**は、ローカルフォームコンテナーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e08e2-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e08e2-119">解説</span><span class="sxs-lookup"><span data-stu-id="e08e2-119">Remarks</span></span>

<span data-ttu-id="e08e2-120">クライアントアプリケーションは、指定されたファイル名を持つファイルに現在のフォームの説明を保存するために、 **imapiforminfo:: saveform**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e08e2-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="e08e2-121">**saveform**構成ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="e08e2-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e08e2-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e08e2-122">Notes to callers</span></span>

<span data-ttu-id="e08e2-123">フォームを再インストールするには、フォームライブラリプロバイダーが表示するダイアログボックスでフォーム記述子メッセージのリストからフォームを選択します。</span><span class="sxs-lookup"><span data-stu-id="e08e2-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="e08e2-124">フォーム記述子メッセージに推奨される拡張子は、fdm です。</span><span class="sxs-lookup"><span data-stu-id="e08e2-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="e08e2-125">**saveform**が MAPI_E_EXTENDED_ERROR を返す場合は、 [imapiprop:: GetLastError](imapiprop-getlasterror.md)メソッドを呼び出し、返された**MAPIERROR**構造を調べて、エラーの原因となった条件を特定します。</span><span class="sxs-lookup"><span data-stu-id="e08e2-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e08e2-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="e08e2-126">See also</span></span>



[<span data-ttu-id="e08e2-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="e08e2-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="e08e2-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="e08e2-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="e08e2-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e08e2-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

