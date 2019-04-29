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
  
[PreprocessMessage](preprocessmessage.md)ベースの関数によって作成された前処理された情報をメッセージから削除します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi  <br/> |
|定義された関数の実装:  <br/> |トランスポートプロバイダー  <br/> |
|によって呼び出された定義済み関数:  <br/> |MAPI スプーラー  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>パラメーター

 _lpmessage_
  
> 順番削除する情報があるプリプロセスされたメッセージへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK
  
> 前処理された情報が正常に削除されました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、 **removepreprocessinfo**に基づいて関数を呼び出します。 トランスポートプロバイダーは、 [imapisupport:: registerpreprocessor プロセッサ](imapisupport-registerpreprocessor.md)メソッドへの呼び出しで、並列**PreprocessMessage**ベースの関数を登録するのと同時に、 **removepreprocessinfo**に基づく関数を登録します。 
  
[PreprocessMessage](preprocessmessage.md)関数プロトタイプによって定義された関数によって書き込まれたプリプロセスされた情報の例として、fax 送信に適したイメージレンダリングがあります。 MAPI スプーラーは、通常、前処理された情報を含むメッセージを送信した後に、 **removepreprocessinfo**関数を呼び出します。 
  

