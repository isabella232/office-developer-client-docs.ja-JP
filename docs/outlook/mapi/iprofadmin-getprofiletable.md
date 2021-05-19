---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2db7dba67e7b71df6921ecd97189255a0ef7823a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414646"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="5a553-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="5a553-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="5a553-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a553-105">使用可能なすべてのプロファイルに関する情報を含むテーブルであるプロファイル テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5a553-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5a553-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5a553-106">Parameters</span></span>

 <span data-ttu-id="5a553-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a553-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5a553-108">[in]常に NULL。</span><span class="sxs-lookup"><span data-stu-id="5a553-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="5a553-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5a553-109">_lppTable_</span></span>
  
> <span data-ttu-id="5a553-110">[out]プロファイル テーブルへのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="5a553-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a553-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="5a553-111">Return value</span></span>

<span data-ttu-id="5a553-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a553-112">S_OK</span></span> 
  
> <span data-ttu-id="5a553-113">プロファイル テーブルが正常に取得されました。</span><span class="sxs-lookup"><span data-stu-id="5a553-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5a553-114">注釈</span><span class="sxs-lookup"><span data-stu-id="5a553-114">Remarks</span></span>

<span data-ttu-id="5a553-115">**IProfAdmin::GetProfileTable** メソッドは、利用可能なプロファイルごとに 1 行を含むプロファイル テーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="5a553-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="5a553-116">各行には、プロファイルの表示名と、プロファイルが既定であるかどうかを示すフラグの 2 つの列があります。</span><span class="sxs-lookup"><span data-stu-id="5a553-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="5a553-117">削除されたプロファイル、または使用されているが削除のマークが付いているプロファイルは、プロファイル テーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="5a553-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="5a553-118">プロファイル テーブルは静的です。以降のプロファイルの追加および削除は、表には反映されません。</span><span class="sxs-lookup"><span data-stu-id="5a553-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="5a553-119">プロファイルが存在しない場合 **、GetProfileTable は** 行が 0 のテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="5a553-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="5a553-120">プロファイル テーブルの詳細については、「Profile [Tables」を参照してください](profile-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="5a553-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5a553-121">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="5a553-121">MFCMAPI reference</span></span>

<span data-ttu-id="5a553-122">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5a553-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5a553-123">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="5a553-123">**File**</span></span>|<span data-ttu-id="5a553-124">**関数**</span><span class="sxs-lookup"><span data-stu-id="5a553-124">**Function**</span></span>|<span data-ttu-id="5a553-125">**コメント**</span><span class="sxs-lookup"><span data-stu-id="5a553-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a553-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5a553-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="5a553-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="5a553-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="5a553-128">MFCMAPI は **、IProfAdmin::GetProfileTable** メソッドを使用して、新しいダイアログ ボックスに表示するプロファイル テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="5a553-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a553-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a553-129">See also</span></span>



[<span data-ttu-id="5a553-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a553-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="5a553-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="5a553-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="5a553-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a553-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="5a553-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="5a553-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

