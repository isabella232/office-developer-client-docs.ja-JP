---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: メールアイテムの PidTagConversationId に基づいて、送信後の分類を実行します。
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318901"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

メールアイテムの[PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)に基づいて、送信後の分類を実行します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|エクスポート対象:  <br/> |outlook.exe  <br/> |
|呼び出し元:  <br/> |クライアント  <br/> |
|実装元:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a>パラメーター

_pmbinStoreEid_
  
> 順番ストアの[PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) 、またはメールアイテムの[PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) 。 NULL または無効にすることはできません。 
    
_pmbinmsgeid_
  
> 順番メールアイテムの[PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) 。 NULL または無効にすることはできません。 
    
_pmbinconvid_
  
> 順番メールアイテムの[PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) 。 NULL または無効にすることはできません。 
    
_dwFlags_
  
> 順番メソッド呼び出しに関する追加情報を指定するビットマスク。
    
   - 0-このメソッド呼び出しでは、追加のオプションは使用されません。 この値を指定することをお勧めします。 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinmsgeid_は、実際にはメッセージの[PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx)です。 **PidTagSearchKey**を使用すると、リソースが大量に消費されるため、 [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)を使用できる場合は回避する必要があります。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
|E_INVALIDARG  <br/> | _dwFlags_に不明なフラグが含まれています。  <br/> |
   
## <a name="remarks"></a>解説

カテゴリは個人情報と見なされるため、ユーザーのメールボックスの外部に送信することはできません。 そのため、未送信のメールアイテムに対して**HrProcessConvActionForSentItem**を呼び出すことはできません。 代わりに、アイテムを送信してから、アーカイブコピーで**HrProcessConvActionForSentItem**を呼び出します。 アーカイブされたコピーは、[送信済みアイテム] フォルダーまたは同等の場所に保存できます。 
  
アプリケーションは、 **HrProcessConvActionForSentItem**を呼び出すために、COM アドインからの場合など、outlook.exe を使用して処理されている必要があります。 プロセス外で**HrProcessConvActionForSentItem**を呼び出そうとすると、 **HrProcessConvActionForSentItem**によってアクセス違反例外がスローされます。 
  

