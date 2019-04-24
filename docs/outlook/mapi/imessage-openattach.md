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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e0c3747b48526b715f976e7bf3c142097c85f29a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349253"
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

 _ulattachmentnum_
  
> 順番添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティに格納されている、開く添付ファイルのインデックス番号を指定します。 このインデックス番号は、メッセージの添付ファイルを一意に識別するもので、メッセージのコンテキストでのみ有効です。
    
 _lpinterface_
  
> 順番添付ファイルへのアクセスに使用するインターフェイスを表すインターフェイス識別子 (IID) へのポインター。 NULL 結果を添付ファイルの標準インターフェイスまたは**iattach**に渡すと、返されます。 
    
 _ulFlags_
  
> 順番添付ファイルを開く方法を制御するフラグのビットマスクです。 次のフラグを設定できます。 
    
MAPI_BEST_ACCESS 
  
> ユーザーに対して許可される最大のネットワークアクセス許可と、クライアントアプリケーションの最大アクセス権を使用して、添付ファイルを開くように要求します。 たとえば、クライアントに読み取り/書き込みアクセス許可がある場合、添付ファイルは読み取り/書き込みアクセス許可を使用して開く必要があります。クライアントが読み取り専用のアクセス権を持っている場合は、添付ファイルを読み取り専用アクセスで開く必要があります。 
    
MAPI_DEFERRED_ERRORS 
  
> 添付ファイルが呼び出し元クライアントに完全に使用可能になる前に、 **openattach**を正常に返すことができるようにします。 添付ファイルを使用できない場合は、その後の呼び出しを行うとエラーが発生する可能性があります。 
    
MAPI_MODIFY 
  
> 読み取り/書き込みアクセス許可を要求します。 既定では、添付ファイルは読み取り専用アクセスで開かれ、読み取り/書き込みアクセス許可が付与されているという前提でクライアントを使用することはできません。 
    
 _lppattach_
  
> 読み上げ開かれた添付ファイルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 添付ファイルが正常に開かれました。
    
## <a name="remarks"></a>解説

**IMessage:: openattach**メソッドは、メッセージの添付ファイルを開きます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

添付ファイルを開くには、添付ファイルの番号または**PR_ATTACH_NUM**プロパティにアクセスできる必要があります。 [IMessage:: getattachmenttable](imessage-getattachmenttable.md)を呼び出して、メッセージの添付ファイルテーブルを取得し、開く添付ファイルを表す行を見つけます。 詳細について[は、「添付ファイルを開く](opening-an-attachment.md)」を参照してください。 
  
1つの添付ファイルを複数回開いてはいけません。結果は未定義で、メッセージストアプロバイダーに依存します。
  
既定の読み取り専用モードではなく、読み取り/書き込みモードで添付ファイルを開くように要求することができます。 ただし、添付ファイルが実際に読み取り/書き込みモードで開かれるかどうかは、メッセージストアプロバイダーによって設定されます。 添付ファイルを変更するか、起こり得るエラーを処理するための準備を試みるか、添付ファイルの**PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) プロパティを取得することによって付与されたアクセスのレベルを確認することができます (使用可能な場合)。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|AttachmentsDlg に使用する  <br/> |CAttachmentsDlg:: openitemprop  <br/> |mfcmapi は、 **IMessage:: openattach**メソッドを使用して添付ファイルオブジェクトを開きます。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMessage: IMAPIProp](imessageimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

