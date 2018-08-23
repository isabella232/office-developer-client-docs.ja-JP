---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7981dc8550485aa22859c4a8dc25541bedf1217c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800879"
---
# <a name="imapiviewcontextgetsavestream"></a>IMAPIViewContext::GetSaveStream

  
  
**適用対象**: Outlook 
  
現在のメッセージを保存するために使用するストリームを取得します。
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a>パラメーター

 _pulFlags_
  
> [out]メッセージ テキストを保存する方法を制御するフラグのビットマスクへのポインター。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> メッセージ文字列は、Unicode 形式で保存されます。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式のテキストが保存されます。
    
 _pulFormat_
  
> [out]保存したテキストの書式を制御するフラグのビットマスクへのポインター。 次のフラグを設定することができます。
    
SAVE_FORMAT_RICHTEXT 
  
> メッセージのテキストは、書式設定されたテキストで、リッチ テキスト形式式 (RTF) として保存するのには。 
    
SAVE_FORMAT_TEXT 
  
> メッセージのテキストは、プレーン テキストとして保存するのには。 
    
 _ppstm_
  
> [out]保存されたメッセージを格納するストリームへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ストリームが正常に取得しました。
    
## <a name="remarks"></a>注釈

フォーム オブジェクトは、ストリーム形式のビューアーで、名前を付けて動詞の処理をサポートするために**IStream**インターフェイスを実装するオブジェクトを取得する**IMAPIViewContext::GetSaveStream**メソッドを呼び出します。 メッセージが完全に適切な文字列形式に変換し、適切なストリームに配置されるまで、 [IMAPIForm::DoVerb](imapiform-doverb.md)メソッドは、フォームのサーバーに実装されているし、動詞を呼び出すフォーム ビューアーによって呼び出されます、する必要があります返されません。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**GetSaveStream**を呼び出す前に_ppstm_で指定されたストリームに書き込みます。 **GetSaveStream**が返されるときは、シーク ポインターの位置はリセットされません。 このポインターは必要があります保存されているメッセージのテキストの最後に残ります。 
  
## <a name="see-also"></a>関連項目



[IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)

