---
title: IMessageOpenAttach
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMessage.OpenAttach
api_type:
- COM
ms.assetid: b680f5a7-0df3-4e7b-bf3b-f149eb42be8d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fa38f1123ab3bd3c13dcad830680e16d5e6d33c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584333"
---
# <a name="imessageopenattach"></a>IMessage::OpenAttach

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
添付ファイルを開きます。 
  
```cpp
HRESULT OpenAttach(
  ULONG ulAttachmentNum,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a>パラメーター

 _ulAttachmentNum_
  
> [in]添付ファイルのプロパティ ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md) **)** プロパティに格納されている、開く添付PR_ATTACH_NUMインデックス番号。 このインデックス番号は、メッセージ内の添付ファイルを一意に識別し、メッセージのコンテキストでのみ有効です。
    
 _lpInterface_
  
> [in]添付ファイルへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL を渡すと、添付ファイルの標準インターフェイス **(IAttach)** が返されます。 
    
 _ulFlags_
  
> [in]添付ファイルの開き方を制御するフラグのビットマスク。 次のフラグを設定できます。 
    
MAPI_BEST_ACCESS 
  
> ユーザーに許可される最大ネットワークアクセス許可と最大クライアント アプリケーション アクセス権を使用して添付ファイルを開く要求。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、添付ファイルを読み取り/書き込みアクセス許可で開く必要があります。クライアントに読み取り専用アクセス権がある場合は、読み取り専用アクセスで添付ファイルを開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> **OpenAttach が正常** に返されるのを許可します。おそらく、添付ファイルが呼び出し元のクライアントで完全に利用できる前に。 添付ファイルを使用できない場合は、後続の呼び出しでエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、添付ファイルは読み取り専用アクセスで開かれません。クライアントは、読み取り/書き込みアクセス許可が付与されているという前提で動作しません。 
    
 _lppAttach_
  
> [out]開いている添付ファイルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 添付ファイルが正常に開かされました。
    
## <a name="remarks"></a>注釈

**IMessage::OpenAttach メソッドは**、メッセージの添付ファイルを開きます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

添付ファイルを開くには、添付ファイル番号または添付ファイルプロパティに **アクセスPR_ATTACH_NUM** 必要があります。 [IMessage::GetAttachmentTable](imessage-getattachmenttable.md)を呼び出して、メッセージの添付ファイル テーブルを取得し、開く添付ファイルを表す行を探します。 詳細 [については、「添付ファイルを開く](opening-an-attachment.md) 」を参照してください。 
  
1 つの添付ファイルを複数回開かれません。結果は未定義であり、メッセージ ストア プロバイダーに依存します。
  
既定の読み取り専用モードではなく、読み取り/書き込みモードで添付ファイルを開く必要があります。 ただし、添付ファイルを実際に読み取り/書き込みモードで開くかどうかは、メッセージ ストア プロバイダーによって異なります。 使用可能な場合は、添付ファイルの変更、エラーの処理の準備、または添付ファイルの **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得して付与されたアクセスのレベルを確認できます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|AttachmentsDlg.cpp 使用する  <br/> |CAttachmentsDlg::OpenItemProp  <br/> |MFCMAPI は **、IMessage::OpenAttach** メソッドを使用して添付ファイル オブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

