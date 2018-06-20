---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 275dc17a141f1c002f62a43824174458e591d4de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800889"
---
# <a name="imessagegetattachmenttable"></a>IMessage::GetAttachmentTable

  
  
**適用されます**: Outlook 
  
メッセージの添付ファイル テーブルを返します。
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]テーブルの作成に関連するフラグのビットマスクです。 次のフラグを設定することができます。 
    
MAPI_UNICODE 
  
> Unicode 形式では、文字列型の列です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に戻す、可能性のあるテーブルが呼び出し側のクライアントに完全に使用する前に**GetAttachmentTable**を使用できます。 テーブルが使用できない場合は、それ以降の呼び出しを行うとエラーが発生することができます。 
    
 _lppTable_
  
> [out]添付ファイル テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 添付ファイル テーブルが正常に取得しました。
    
## <a name="remarks"></a>備考

**IMessage::GetAttachmentTable**メソッドは、メッセージ内のすべての添付ファイルに関する情報が含まれています、メッセージの添付ファイル テーブルにポインターを返します。 クライアントは、添付ファイル テーブルを介してのみ添付ファイルへのアクセスを取得できます。 添付ファイルの数を取得することによって**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティは、クライアントが使用できる**IMessage**の方法のいくつかの添付ファイルを操作します。 
  
添付ファイルごとに 1 つの行があります。 添付ファイル テーブル内の列の一覧は、[添付ファイル テーブル](attachment-tables.md)を参照してください。
  
添付ファイル通常はテーブルに表示されない、添付ファイル[IMAPIProp::SaveChanges](imapiprop-savechanges.md)への呼び出しで、添付ファイルとメッセージの両方が保存されるまでです。 添付ファイル テーブルでは、動的です。 クライアントは新しい添付ファイルを作成、既存の添付ファイルを削除、または 1 つまたは複数のプロパティを変更したら、 **SaveChanges**の呼び出し、メッセージの添付ファイルを場合添付ファイル テーブルが新しい情報を反映するように更新されます。 
  
いくつかの添付ファイル テーブルのサポートまで、さまざまな制限です。そうでないです。 制限のサポートは、メッセージ ストア プロバイダーの実装に依存します。 
  
最初に開くと、添付ファイル テーブルは必ずしも並べ替えられていない特定の順序で。 
  
_UlFlags_パラメーターに MAPI_UNICODE フラグを設定すると、添付ファイル テーブルに次の呼び出しが影響します。 
  
- 列を取得する[IMAPITable::QueryColumns](imapitable-querycolumns.md)を設定します。 
    
- [IMAPITable::QueryRows](imapitable-queryrows.md)の行を取得します。 
    
- 並べ替え順序を取得するために[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)をします。 
    
これらの呼び出しから返される文字列の列の情報は、Unicode 形式である Unicode フラグの要求を設定します。 ただし、Unicode をサポートしていないすべてのメッセージ ストア プロバイダーであるためこのフラグを設定、のみ要求です。
  
## <a name="see-also"></a>関連項目



[IMessage::CreateAttach](imessage-createattach.md)
  
[IMessage::DeleteAttach](imessage-deleteattach.md)
  
[IMessage::OpenAttach](imessage-openattach.md)
  
[IMessage: IMAPIProp](imessageimapiprop.md)

