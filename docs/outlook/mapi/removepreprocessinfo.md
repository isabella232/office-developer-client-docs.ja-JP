---
title: RemovePreprocessInfo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.RemovePreprocessInfo
api_type:
- COM
ms.assetid: 25f46937-abac-4a0b-83db-eeac9451c112
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d80c73aef780a0da39f3939f71462488a067de5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432948"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[PreprocessMessage](preprocessmessage.md)ベースの関数によって書き込まれた前処理済みの情報をメッセージから削除します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|定義された関数は、次の方法で実装されます。  <br/> |トランスポート プロバイダー  <br/> |
|によって呼び出される定義済み関数:  <br/> |MAPI スプーラー  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>パラメーター

 _lpMessage_
  
> [in]情報を削除する処理済みメッセージへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK
  
> 前処理された情報は正常に削除されました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは **、RemovePreprocessInfo に基づいて関数を呼び出します**。 トランスポート プロバイダーは [、IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)メソッドへの呼び出しで並列 **PreprocessMessage** ベースの関数を登録すると同時に、RemovePreprocessInfo ベースの関数を登録します。  
  
FAX 送信に適したイメージ レンダリングは [、PreprocessMessage](preprocessmessage.md)関数プロトタイプによって定義された関数によって書き込まれる前処理済み情報の例です。 MAPI スプーラーは、通常、前処理された情報を含むメッセージを送信した後 **、RemovePreprocessInfo** 関数を呼び出します。 
  

