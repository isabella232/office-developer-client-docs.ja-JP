---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c702e4063bf5e5a06a9e476a02172a780c7e326a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800892"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**適用されます**: Outlook 
  
添付ファイルを開きます。 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>Parameters

 _ulAttachmentNum_
  
> [in]開くには、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティに格納されている添付ファイルのインデックス番号です。 このインデックス番号を一意に、メッセージの添付ファイルを識別し、メッセージのコンテキストでのみ有効です。
    
 _lpInterface_
  
> [in]添付ファイルにアクセスするために使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 パラメーターに NULL が返される添付ファイルの標準的なインタ フェース、または**IAttach**、発生します。 
    
 _ulFlags_
  
> [in]添付ファイルを開く方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
MAPI_BEST_ACCESS 
  
> ユーザーおよび最大のクライアント アプリケーションへのアクセスに使用される最大ネットワークのアクセス許可を持つ添付ファイルを開くことを要求します。 たとえば、クライアントに読み取り/書き込み権限がある場合は、添付ファイル開く必要があります読み取り/書き込みアクセス許可を持つクライアントに読み取り専用アクセスがある場合は、読み取り専用アクセス権を持つ添付ファイルを開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> 正常に戻す、可能性のある添付ファイルは、呼び出し側のクライアントに完全に利用できる前に**OpenAttach**を使用できます。 添付ファイルが利用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。 
    
MAPI_MODIFY 
  
> 要求の読み取り/書き込みのアクセス許可 既定では、添付ファイルは、読み取り専用アクセスで開くし、クライアントが読み取り/書き込みアクセス許可が付与されていることを前提に動作しない必要があります。 
    
 _lppAttach_
  
> [out]開いている添付ファイルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 添付ファイルが正常に開かれました。
    
## <a name="remarks"></a>備考

**IMessage::OpenAttach**メソッドは、メッセージの添付ファイルを開きます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

添付ファイルを開くには、その添付ファイルの数や**PR_ATTACH_NUM**のプロパティへのアクセスが必要です。 メッセージの添付ファイル テーブルを取得し、添付ファイルを開くことを表す行を探し、 [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)を呼び出します。 詳細については、[添付ファイルを開く](opening-an-attachment.md)を参照してください。 
  
複数回 1 つの添付ファイルを開くしないでください。結果は不定であり、メッセージ ストア プロバイダーに依存しているです。
  
添付ファイルは、既定の読み取り専用モードではなく、読み取り/書き込みモードで開くことを要求することができます。 ただし、添付ファイルは実際には、開かれているか読み取り/書き込みモードでは、メッセージ ストア プロバイダーです。 できます、添付ファイルを変更しようとすると、可能性のある障害を処理または使用可能になる場合、添付ファイルの**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) のプロパティを取得することによって付与されたアクセスのレベルを確認する準備をしています。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp をするために使用  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI を開くには、添付ファイルのオブジェクトの**IMessage::OpenAttach**メソッドを使用してください。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

