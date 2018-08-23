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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c90b569414c1710cc1065fdb4fd72738e265ebff
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588833"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
削除は、メッセージから、 [PreprocessMessage](preprocessmessage.md)ベースの関数によって書き込まれた情報をプリプロセスします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapispi.h  <br/> |
|によって実装される関数の定義:  <br/> |トランスポート プロバイダー  <br/> |
|によって呼び出される関数を定義します。  <br/> |MAPI スプーラー  <br/> |
   
```cpp
HRESULT RemovePreprocessInfo(
  LPMESSAGE lpMessage
);
```

## <a name="parameters"></a>パラメーター

 _lpMessage_
  
> [in]削除する元となる情報は、プリプロセス済みのメッセージへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> プリプロセス済みの情報が正常に削除されました。
    
## <a name="remarks"></a>注釈

MAPI スプーラーは、 **RemovePreprocessInfo**に基づく関数を呼び出します。 トランスポート プロバイダーは、同時並行の**PreprocessMessage**ベースの関数を登録するときに、 [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)メソッドの呼び出しで**RemovePreprocessInfo**ベースの関数を登録します。 
  
Fax 転送のための適切なレンダリング イメージは、 [PreprocessMessage](preprocessmessage.md)関数のプロトタイプで定義された関数が記述したプリプロセス済みの情報の例です。 通常、MAPI スプーラーは、プリプロセス済みの情報を含むメッセージを送信した後は**RemovePreprocessInfo**関数を呼び出します。 
  

