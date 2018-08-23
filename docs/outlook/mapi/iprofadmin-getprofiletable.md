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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8b1b037cf24c1bb5a0c84da3d59892ab15763f37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588245"
---
# <a name="iprofadmingetprofiletable"></a><span data-ttu-id="24aee-103">IProfAdmin::GetProfileTable</span><span class="sxs-lookup"><span data-stu-id="24aee-103">IProfAdmin::GetProfileTable</span></span>

  
  
<span data-ttu-id="24aee-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24aee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24aee-105">プロファイル テーブルのすべての利用可能なプロファイルに関する情報を格納するテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="24aee-105">Provides access to the profile table, a table that contains information about all of the available profiles.</span></span>
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="24aee-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="24aee-106">Parameters</span></span>

 <span data-ttu-id="24aee-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="24aee-107">_ulFlags_</span></span>
  
> <span data-ttu-id="24aee-108">[in]常に NULL を返します。</span><span class="sxs-lookup"><span data-stu-id="24aee-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="24aee-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="24aee-109">_lppTable_</span></span>
  
> <span data-ttu-id="24aee-110">[out]プロファイル テーブルへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="24aee-110">[out] A pointer to a pointer to the profile table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="24aee-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="24aee-111">Return value</span></span>

<span data-ttu-id="24aee-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="24aee-112">S_OK</span></span> 
  
> <span data-ttu-id="24aee-113">プロファイル テーブルが正常に取得しました。</span><span class="sxs-lookup"><span data-stu-id="24aee-113">The profile table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24aee-114">注釈</span><span class="sxs-lookup"><span data-stu-id="24aee-114">Remarks</span></span>

<span data-ttu-id="24aee-115">**IProfAdmin::GetProfileTable**メソッドは、すべての利用可能なプロファイルの 1 つの行が含まれているプロファイルのテーブルへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="24aee-115">The **IProfAdmin::GetProfileTable** method provides access to the profile table, which contains one row for every available profile.</span></span> <span data-ttu-id="24aee-116">各行の 2 つの列がある: プロファイルの表示名、およびプロファイルが既定値であるかどうかを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="24aee-116">There are only two columns in each row: the profile's display name, and a flag that indicates whether the profile is the default.</span></span> 
  
<span data-ttu-id="24aee-117">プロファイルが削除されている、またはを使用しているが、削除対象としてマークされている、プロファイル テーブルには含まれません。</span><span class="sxs-lookup"><span data-stu-id="24aee-117">Profiles that have been deleted, or that are in use but have been marked for deletion, are not included in the profile table.</span></span> <span data-ttu-id="24aee-118">プロファイル テーブルは静的です。テーブルでは、プロファイルの後の追加と削除は反映されません。</span><span class="sxs-lookup"><span data-stu-id="24aee-118">The profile table is static; subsequent additions and deletions of profiles are not reflected in the table.</span></span> 
  
<span data-ttu-id="24aee-119">プロファイルが存在しない場合、 **GetProfileTable**は、0 個の行を持つテーブルを返します。</span><span class="sxs-lookup"><span data-stu-id="24aee-119">If no profiles exist, **GetProfileTable** returns a table with zero rows.</span></span> 
  
<span data-ttu-id="24aee-120">プロファイル テーブルの詳細については、[プロファイル テーブル](profile-tables.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="24aee-120">For more information about the profile table, see [Profile Tables](profile-tables.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="24aee-121">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="24aee-121">MFCMAPI reference</span></span>

<span data-ttu-id="24aee-122">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="24aee-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="24aee-123">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="24aee-123">**File**</span></span>|<span data-ttu-id="24aee-124">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="24aee-124">**Function**</span></span>|<span data-ttu-id="24aee-125">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="24aee-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24aee-126">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="24aee-126">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="24aee-127">CMainDlg::OnShowProfiles</span><span class="sxs-lookup"><span data-stu-id="24aee-127">CMainDlg::OnShowProfiles</span></span>  <br/> |<span data-ttu-id="24aee-128">MFCMAPI では、 **IProfAdmin::GetProfileTable**メソッドを使用して、新しいダイアログ ボックスに表示するプロファイル テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="24aee-128">MFCMAPI uses the **IProfAdmin::GetProfileTable** method to get the profile table to display in a new dialog box.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="24aee-129">関連項目</span><span class="sxs-lookup"><span data-stu-id="24aee-129">See also</span></span>



[<span data-ttu-id="24aee-130">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24aee-130">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="24aee-131">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="24aee-131">MAPILogonEx</span></span>](mapilogonex.md)
  
[<span data-ttu-id="24aee-132">IProfAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="24aee-132">IProfAdmin : IUnknown</span></span>](iprofadminiunknown.md)


<span data-ttu-id="24aee-133">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="24aee-133">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

