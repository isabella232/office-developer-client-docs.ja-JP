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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: fab8860621cee5a87b087ee9d98f373baa278e45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803772"
---
# <a name="removepreprocessinfo"></a>RemovePreprocessInfo

  
  
**適用されます**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _lpMessage_
  
> [in]削除する元となる情報は、プリプロセス済みのメッセージへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK
  
> プリプロセス済みの情報が正常に削除されました。
    
## <a name="remarks"></a>備考

MAPI スプーラーは、 **RemovePreprocessInfo**に基づく関数を呼び出します。 トランスポート プロバイダーは、同時並行の**PreprocessMessage**ベースの関数を登録するときに、 [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md)メソッドの呼び出しで**RemovePreprocessInfo**ベースの関数を登録します。 
  
Fax 転送のための適切なレンダリング イメージは、 [PreprocessMessage](preprocessmessage.md)関数のプロトタイプで定義された関数が記述したプリプロセス済みの情報の例です。 通常、MAPI スプーラーは、プリプロセス済みの情報を含むメッセージを送信した後は**RemovePreprocessInfo**関数を呼び出します。 
  

