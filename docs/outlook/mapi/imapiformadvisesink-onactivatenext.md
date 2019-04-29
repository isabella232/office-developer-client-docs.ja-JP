---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d647b41018afbade91dffb2818b48b0738148855
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411765"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームが次に表示されるメッセージのメッセージクラスを処理できるかどうかを示します。
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>パラメーター

 _lpszmessageclass_
  
> 順番次のメッセージのメッセージクラスへのポインター。
    
 _ulmessagestatus_
  
> 順番メッセージが含まれる contents テーブルに関する状態情報を提供する、クライアント定義またはプロバイダー定義のフラグのビットマスク。これは、表示する次のメッセージの**PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされます。順番.
    
 _ulmessageflags_
  
> 順番メッセージの現在の状態を示す次のメッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。
    
 _pppersistmessage_
  
> 読み上げ新しいフォームが必要な場合は、新しいフォームに使用される form オブジェクトの[IPersistMessage](ipersistmessageiunknown.md)実装へのポインターへのポインター。 現在の form オブジェクトを使用して次のメッセージを表示し保存できる場合は、NULL へのポインターが返されます。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知は正常に実行され、フォームは次のメッセージを処理することができます。
    
S_FALSE 
  
> フォームでは、次のメッセージのメッセージクラスは処理されません。
    
## <a name="remarks"></a>注釈

フォームビューアーは、 **IMAPIFormAdviseSink:: OnActivateNext**メソッドを呼び出して、フォームが次のメッセージをフォルダー内に表示できるかどうかを判断できるようにします。 次のメッセージは任意のクラスのメッセージである可能性がありますが、通常は同じクラスまたは関連クラスのものです。 これにより、クライアントアプリケーションが可能な限りフォームオブジェクトを再利用できるようにすることで、同じクラスの複数のメッセージをより効率的に読み取ることができます。 
  
ほとんどの form オブジェクトは、 _lpszmessageclass_パラメーターで指定されたメッセージクラスを使用して、次のメッセージを処理できるかどうかを判断します。 通常、フォームは、既定のクラスに属するメッセージに加えて、フォームの既定のクラスがサブクラスであるクラスに属するメッセージを処理できます。 ただし、フォームで他の要素を使用して、メッセージを処理できるかどうか (次のメッセージの送信済みまたは未送信の状態など) を確認することはできません。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームがメッセージクラスを処理できる場合は、 _pppersistmessage_パラメーターで S_OK および NULL を返します。 フォームで処理できないメッセージを処理できる新しいフォームを作成できる場合は、次の手順を実行します。 
  
1. フォームのクラスファクトリを呼び出して、新しい form オブジェクトのインスタンスを作成します。
    
2. そのインスタンスを_pppersistmessage_ポインターパラメーターの内容に格納します。 
    
3. S_OK ��Ԃ��܂��B
    
フォームビューアーは、 _pppersistmessage_が指すオブジェクトに属する[IPersistMessage:: load](ipersistmessage-load.md)メソッドを使用して、メッセージを読み込みます。
  
作成できるフォームまたはフォームのいずれも、次のメッセージを処理できる場合は、S_FALSE を返します。 ただし、一般に、フォームビューアーのパフォーマンスが低下する原因となるため、フォームはこの値を返さないようにする必要があります。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions  <br/> |cmymapiformviewer:: ActivateNext  <br/> |mfcmapi は、 **IMAPIFormAdviseSink:: OnActivateNext**メソッドを使用して、 [imapiviewcontext:: ActivateNext](imapiviewcontext-activatenext.md)メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

