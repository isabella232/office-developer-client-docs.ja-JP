---
title: IMAPIFormAdviseSinkOnActivateNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFormAdviseSink.OnActivateNext
api_type:
- COM
ms.assetid: db621dfd-c6ad-42d2-8089-db40a63cab36
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 8cf28a3c5b6cdcfc8873a9613ac1fef2b5e7640a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579930"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表示する次のメッセージのメッセージ クラスをフォームで処理できるかどうかを示します。
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>パラメーター

 _lpszMessageClass_
  
> [in]次のメッセージのメッセージ クラスへのポインター。
    
 _ulMessageStatus_
  
> [in]次に表示するメッセージ **の PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) プロパティからコピーされたクライアント定義フラグまたはプロバイダー定義フラグのビットマスクで、メッセージが含まれるコンテンツ テーブルに関する状態情報を提供します。
    
 _ulMessageFlags_
  
> [in]メッセージの現在の状態を示す次のメッセージの **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティからコピーされたフラグのビットマスクへのポインター。
    
 _ppPersistMessage_
  
> [out]新しいフォームが必要な場合に、新しいフォームに使用されるフォーム オブジェクトの [IPersistMessage](ipersistmessageiunknown.md) 実装へのポインター。 現在のフォーム オブジェクトを使用して次のメッセージを表示および保存できる場合は、NULL へのポインターを返します。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 通知が成功し、フォームは次のメッセージを処理できます。
    
S_FALSE 
  
> フォームは、次のメッセージのメッセージ クラスを処理します。
    
## <a name="remarks"></a>注釈

フォーム ビューアーは **IMAPIFormAdviseSink::OnActivateNext** メソッドを呼び出して、フォルダー内に次のメッセージを表示できるかどうかをフォームが判断するのに役立ちます。 次のメッセージは、任意のクラスのメッセージである可能性がありますが、通常は同じクラスまたは関連するクラスです。 これにより、クライアント アプリケーションが可能な限りフォーム オブジェクトを再利用することで、同じクラスの複数のメッセージを読み取るプロセスが効率的になります。 
  
ほとんどのフォーム オブジェクトは  _、lpszMessageClass_ パラメーターが指すメッセージ クラスを使用して、次のメッセージを処理できるかどうかを判断します。 通常、フォームは、既定のクラスに属するメッセージに加えて、フォームの既定のクラスがサブクラスであるクラスに属するメッセージを処理できます。 ただし、フォームは他の要素を使用して、次のメッセージの送信済み状態や送信されていない状態など、メッセージを処理できるかどうかを疑問なく判断できます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

フォームS_OKメッセージ クラスを処理できる場合は  _、ppPersistMessage_ パラメーターの値と NULL を返します。 フォームで処理できないメッセージを処理できる新しいフォームを作成できる場合は、次の手順を実行します。 
  
1. フォームのクラス ファクトリを呼び出して、新しいフォーム オブジェクトのインスタンスを作成します。
    
2. そのインスタンスを  _ppPersistMessage_ ポインター パラメーターの内容に格納します。 
    
3. S_OK ��Ԃ��܂��B
    
フォーム ビューアーは _、ppPersistMessage_ が指すオブジェクトに属する [IPersistMessage::Load](ipersistmessage-load.md)メソッドを使用してメッセージを読み込む。
  
作成できるフォームもフォームも次のメッセージを処理しない場合は、次のメッセージをS_FALSE。 ただし、フォーム ビューアーのパフォーマンスが低下する原因となるので、一般に、フォームはこの値を返す必要があります。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI は **IMAPIFormAdviseSink::OnActivateNext** メソッドを使用して [IMAPIViewContext::ActivateNext メソッドを実装](imapiviewcontext-activatenext.md) します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage : IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[PidTagMessageFlags 標準プロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus 標準プロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink : IUnknown](imapiformadvisesinkiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

