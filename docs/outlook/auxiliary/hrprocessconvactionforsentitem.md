---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: PidTagConversationId に基づいてメール アイテムに対して送信後の分類を実行します。
ms.openlocfilehash: 45f1aa9dbab683fb6765d637b8495d77d899fbe2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614456"
---
# <a name="hrprocessconvactionforsentitem"></a>HrProcessConvActionForSentItem

[PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)に基づいてメール アイテムに対して送信後の分類を実行します。
  
## <a name="quick-info"></a>クイック ヒント

|||
|:-----|:-----|
|次の方法でエクスポートされます。  <br/> |Outlook.exe  <br/> |
|呼び出し元:  <br/> |Client  <br/> |
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
  
> [in]ストア[の PidTagEntryId、](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)またはメール[アイテムの PidTagStoreEntryId。](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) NULL または無効にすることはできません。 
    
_pmbinMsgEid_
  
> [in]メール[アイテムの PidTagEntryId。](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) NULL または無効にすることはできません。 
    
_pmbinConvID_
  
> [in]メール[アイテムの PidTagConversationId。](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) NULL または無効にすることはできません。 
    
_dwFlags_
  
> [in]メソッド呼び出しに関する追加情報を指定するビットマスク。
    
   - 0 - このメソッド呼び出しでは、追加のオプションは使用されません。 これは推奨される値です。 
    
   - **PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ は、実際には [メッセージの PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) です。 **PidTagSearchKey** の使用はリソースの負荷が高く [、PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)が使用可能な場合は避ける必要があります。 
    
## <a name="return-values"></a>戻り値

|**HRESULT 型**|**Description**|
|:-----|:-----|
|S_OK  <br/> |呼び出しが正常になされました。  <br/> |
|E_INVALIDARG  <br/> | _dwFlags には_ 不明なフラグが含まれている。  <br/> |
   
## <a name="remarks"></a>注釈

カテゴリは個人情報と見なされ、ユーザーのメールボックスの外部に送信される必要があります。 したがって、送信されていないメール アイテム **に対して HrProcessConvActionForSentItem** を呼び出す必要があります。 代わりに、アイテムを送信し、アーカイブされたコピーで **HrProcessConvActionForSentItem** を呼び出します。 アーカイブされたコピーは、[送信済みアイテム] フォルダーまたは同等の場所に保存できます。 
  
**HrProcessConvActionForSentItem** を呼び出Outlook.exe COM アドインなど、アプリケーションがプロセス内にある必要があります。 **HrProcessConvActionForSentItem** をアウトプロセスで呼び出す場合 **、HrProcessConvActionForSentItem** はアクセス違反例外をスローします。 
  

