---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7de404f421a405d80dd7f98beba5168969222fc9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800691"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="497fa-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="497fa-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="497fa-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="497fa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="497fa-105">ステータス テーブル、セッション内のすべての MAPI リソースに関する情報が含まれているテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="497fa-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="497fa-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="497fa-106">Parameters</span></span>

 <span data-ttu-id="497fa-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="497fa-107">_ulFlags_</span></span>
  
> <span data-ttu-id="497fa-108">[in]文字の文字列の列の形式を決定するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="497fa-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="497fa-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="497fa-109">The following flag can be set:</span></span>
    
<span data-ttu-id="497fa-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="497fa-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="497fa-111">Unicode 形式では、文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="497fa-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="497fa-112">MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。</span><span class="sxs-lookup"><span data-stu-id="497fa-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="497fa-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="497fa-113">_lppTable_</span></span>
  
> <span data-ttu-id="497fa-114">[out]ステータス テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="497fa-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="497fa-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="497fa-115">Return value</span></span>

<span data-ttu-id="497fa-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="497fa-116">S_OK</span></span> 
  
> <span data-ttu-id="497fa-117">テーブルが正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="497fa-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="497fa-118">注釈</span><span class="sxs-lookup"><span data-stu-id="497fa-118">Remarks</span></span>

<span data-ttu-id="497fa-119">**IMAPISession::GetStatusTable**メソッドは、セッション内のすべての MAPI リソースに関する情報を含むステータス テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="497fa-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="497fa-120">MAPI サブシステムについての情報のテーブルの 1 行、1 行、MAPI スプーラーを無効、統合アドレス帳の 1 つの行とプロファイルには、各サービス プロバイダーの 1 つの行があります。</span><span class="sxs-lookup"><span data-stu-id="497fa-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="497fa-121">状態テーブル内の必須および省略可能な列の一覧については、[ステータス ・ テーブル](status-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="497fa-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="497fa-122">_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。</span><span class="sxs-lookup"><span data-stu-id="497fa-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="497fa-123">このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。</span><span class="sxs-lookup"><span data-stu-id="497fa-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="497fa-124">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="497fa-124">MFCMAPI reference</span></span>

<span data-ttu-id="497fa-125">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="497fa-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="497fa-126">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="497fa-126">**File**</span></span>|<span data-ttu-id="497fa-127">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="497fa-127">**Function**</span></span>|<span data-ttu-id="497fa-128">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="497fa-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="497fa-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="497fa-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="497fa-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="497fa-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="497fa-131">MFCMAPI では、 **IMAPISession::GetStatusTable**メソッドを使用してレンダリングされる状態のテーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="497fa-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="497fa-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="497fa-132">See also</span></span>



[<span data-ttu-id="497fa-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="497fa-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="497fa-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="497fa-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="497fa-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="497fa-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="497fa-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="497fa-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="497fa-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="497fa-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="497fa-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="497fa-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="497fa-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="497fa-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


<span data-ttu-id="497fa-140">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="497fa-140">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>
  
[<span data-ttu-id="497fa-141">状態テーブル</span><span class="sxs-lookup"><span data-stu-id="497fa-141">Status Tables</span></span>](status-tables.md)

