---
title: IMAPIFormInfoSaveForm
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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428747"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="8933a-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="8933a-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="8933a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8933a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8933a-105">特定のフォームの説明を構成ファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="8933a-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="8933a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="8933a-106">Parameters</span></span>

 <span data-ttu-id="8933a-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="8933a-107">_szFileName_</span></span>
  
> <span data-ttu-id="8933a-108">[in]説明が保存されているフォームの説明メッセージ ファイルの名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="8933a-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="8933a-109">このファイル名には、拡張子 .fdm が必要です。</span><span class="sxs-lookup"><span data-stu-id="8933a-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8933a-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="8933a-110">Return value</span></span>

<span data-ttu-id="8933a-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="8933a-111">S_OK</span></span> 
  
> <span data-ttu-id="8933a-112">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="8933a-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="8933a-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="8933a-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="8933a-114">構成ファイルを書き込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="8933a-114">The configuration file could not be written.</span></span> <span data-ttu-id="8933a-115">エラーに関連 [付けられている MAPIERROR](mapierror.md) 構造を取得するには [、IMAPIProp::GetLastError メソッドを呼び出](imapiprop-getlasterror.md) します。</span><span class="sxs-lookup"><span data-stu-id="8933a-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="8933a-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="8933a-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="8933a-117">ローカル フォーム コンテナーにフォームを保存するために **SaveForm** が呼び出された可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8933a-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="8933a-118">**SaveForm** はローカル フォーム コンテナーではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8933a-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8933a-119">注釈</span><span class="sxs-lookup"><span data-stu-id="8933a-119">Remarks</span></span>

<span data-ttu-id="8933a-120">クライアント アプリケーションは **IMAPIFormInfo::SaveForm** メソッドを呼び出して、指定されたファイル名を持つファイルに現在のフォームの説明を保存します。</span><span class="sxs-lookup"><span data-stu-id="8933a-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="8933a-121">**SaveForm** は構成ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="8933a-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8933a-122">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="8933a-122">Notes to callers</span></span>

<span data-ttu-id="8933a-123">フォームを再インストールするには、フォーム ライブラリ プロバイダーが表示するダイアログ ボックスのフォーム記述子メッセージの一覧からフォームを選択します。</span><span class="sxs-lookup"><span data-stu-id="8933a-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="8933a-124">フォーム記述子メッセージの推奨拡張機能は .fdm です。</span><span class="sxs-lookup"><span data-stu-id="8933a-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="8933a-125">**SaveForm** が MAPI_E_EXTENDED_ERROR を返す場合は [IMAPIProp::GetLastError](imapiprop-getlasterror.md)メソッドを呼び出し、返された **MAPIERROR** 構造体をチェックして、エラーの原因となる条件を特定します。</span><span class="sxs-lookup"><span data-stu-id="8933a-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8933a-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="8933a-126">See also</span></span>



[<span data-ttu-id="8933a-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8933a-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="8933a-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="8933a-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="8933a-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8933a-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

