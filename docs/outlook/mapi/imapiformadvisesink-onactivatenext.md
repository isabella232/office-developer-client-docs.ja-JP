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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 3ce4d57ab4837f40ffbc898fde68e44cc802676f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800504"
---
# <a name="imapiformadvisesinkonactivatenext"></a>IMAPIFormAdviseSink::OnActivateNext

  
  
**適用されます**: Outlook 
  
フォームを表示するのには、次のメッセージのメッセージ クラスを処理できるかどうかを示します。
  
```cpp
HRESULT OnActivateNext(
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPPERSISTMESSAGE FAR * ppPersistMessage
);
```

## <a name="parameters"></a>Parameters

 _lpszMessageClass_
  
> [in]次のメッセージのメッセージ クラスへのポインター。
    
 _ulMessageStatus_
  
> [in]メッセージが含まれているコンテンツのテーブルに関するステータス情報を提供する、 **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) のプロパティを表示するには、次のメッセージからコピーされた、クライアントが定義されているか、プロバイダーで定義されているフラグのビットマスクします。
    
 _ulMessageFlags_
  
> [in]フラグは、 **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) のプロパティを表示するのには、次のメッセージからコピーのビットマップへのポインターでは、メッセージの現在の状態を示します。
    
 _ppPersistMessage_
  
> [out][IPersistMessage](ipersistmessageiunknown.md)の実装の新しいフォームで、新しいフォームが必要な場合に使用されるフォーム オブジェクトへのポインターへのポインター。 表示し、次のメッセージを保存する、現在のフォームを使用できる場合、NULL へのポインターを返すことができます。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 通知が成功し、フォームは、次のメッセージを処理できます。
    
S_FALSE 
  
> フォームでは、次のメッセージのメッセージ クラスは処理されません。
    
## <a name="remarks"></a>備考

フォームの閲覧者は、フォルダー内の次のメッセージを表示できるかどうかを決定するフォームのために**IMAPIFormAdviseSink::OnActivateNext**メソッドを呼び出します。 次のメッセージは、任意のクラスのメッセージである可能性がありますが、通常同じクラスの関連するクラスです。 こうと、可能な場合、フォーム オブジェクトを再利用するクライアント アプリケーションを有効にするとより効率的な同じクラスの複数のメッセージを読み取って処理します。 
  
フォームのほとんどのオブジェクトは次のメッセージを処理できるかどうかを判断するのには、 _lpszMessageClass_パラメーターで指定されたメッセージ クラスを使用します。 通常、フォームは、フォームの既定のクラスが既定のクラスに属しているメッセージだけでなく、サブクラスがクラスに属しているメッセージを処理できます。 ただし、フォームでは、質問しないかどうか、メッセージの処理、次のメッセージの送信または未送信の状態などを決定するのにその他の要因を使用できます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

フォームは、メッセージ クラスを処理できる場合、 _ppPersistMessage_パラメーターに S_OK と NULL を返します。 フォームは、フォームが処理することがあるメッセージを処理できる新しいフォームを作成できます、以下の手順を実行します。 
  
1. 新しいフォーム オブジェクトのインスタンスを作成するのには、フォームのクラス ファクトリを呼び出します。
    
2. _PpPersistMessage_ポインター パラメーターの内容でそのインスタンスを格納します。 
    
3. S_OK ��Ԃ��܂��B
    
フォーム ビューアーは、メッセージを_ppPersistMessage_が指すオブジェクトが所属する[IPersistMessage::Load](ipersistmessage-load.md)メソッドを使用して読み込まれます。
  
フォームも作成できるフォームには、次のメッセージが処理される場合は、S_FALSE を返します。 ただし、一般に、フォームを返さないでくださいこの値に発生するためは、フォームのビューアーでのパフォーマンスを低下します。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |CMyMAPIFormViewer::ActivateNext  <br/> |MFCMAPI では、 **IMAPIFormAdviseSink::OnActivateNext**メソッドを使用して、 [IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)メソッドを実装します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPIViewContext::ActivateNext](imapiviewcontext-activatenext.md)
  
[IPersistMessage: IUnknown](ipersistmessageiunknown.md)
  
[IPersistMessage::Load](ipersistmessage-load.md)
  
[PidTagMessageFlags の標準的なプロパティ](pidtagmessageflags-canonical-property.md)
  
[PidTagMessageStatus の標準的なプロパティ](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormAdviseSink: IUnknown](imapiformadvisesinkiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
