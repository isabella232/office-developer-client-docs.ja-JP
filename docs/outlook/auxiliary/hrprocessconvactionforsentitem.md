---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: その PidTagConversationId のメール アイテムの送信の後の分類を実行します。
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799331"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

その[PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)のメール アイテムの送信の後の分類を実行します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|によってエクスポートされます。  <br/> |Outlook.exe  <br/> |
|によって呼び出されます。  <br/> |クライアント  <br/> |
|によって実装されます。  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>パラメーター

_pmbinStoreEid_
  
> [in]ストア、またはメール アイテムの[PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx)の[PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)です。 できませんが NULL または無効です。 
    
_pmbinMsgEid_
  
> [in]メール アイテムの[PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) 。 できませんが NULL または無効です。 
    
_pmbinConvID_
  
> [in]メール アイテムの[PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) 。 できませんが NULL または無効です。 
    
_dwFlags_
  
> [in]メソッドの呼び出しに関する追加情報を指定するビットマスク。
    
   - 0: このメソッドの呼び出しで追加のオプションは使用されません。 これは、推奨される値です。 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**- _pmbinMsgEid_は、実際には、 [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx)のメッセージです。 の**PidTagSearchKey**を使用してリソース集中型ではの[PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)がある場合は避ける必要があります。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_には、不明なフラグが含まれています。  <br/> |
   
## <a name="remarks"></a>注釈

カテゴリでは、個人情報と見なされます、ユーザーのメールボックス以外の場所は転送されません。 したがって、 **HrProcessConvActionForSentItem**をは、未送信のメール アイテムには呼び出さないようにしてください。 代わりに、アイテムを送信し、アーカイブされたコピーで**HrProcessConvActionForSentItem**を呼び出します。 アーカイブされたコピーは、送信済みアイテム フォルダー、または同等の場所に格納されている可能性があります。 
  
アプリケーションはプロセス内である必要があります Outlook.exe など、COM アドイン、 **HrProcessConvActionForSentItem**を呼び出すとします。 **HrProcessConvActionForSentItem**アウト プロセスの呼び出しを試みると、 **HrProcessConvActionForSentItem**は、アクセス違反の例外をスローします。 
  

