---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 681fd68fc068633912df1cb7f060b8c4111b5de8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566538"
---
# <a name="imsgstoregetreceivefoldertable"></a>IMsgStore::GetReceiveFolderTable

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
受信フォルダーのテーブルのすべてのメッセージ ストアの受信フォルダーに関する情報が含まれるテーブルへのアクセスを提供します。
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]テーブルのアクセスを制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_DEFERRED_ERRORS 
  
> 正常に戻す、可能性のあるテーブルは、呼び出し元に完全に利用できる前に**GetReceiveFolderTable**を使用できます。 テーブルを完全に使用できない場合は、テーブルのそれ以降の呼び出しを行うとエラーが発生します。 
    
MAPI_UNICODE 
  
> 関数が返す文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。
    
 _lppTable_
  
> [out]フォルダーの受信表へのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 受信フォルダーのテーブルが正常に返されました。
    
## <a name="remarks"></a>注釈

**IMsgStore::GetReceiveFolderTable**メソッドは、すべてのメッセージ ストアのプロパティの設定値が表示されるフォルダーを表示するテーブルへのアクセスを提供します。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

受信フォルダー テーブルで必要な列の一覧、[フォルダーのテーブルに表示される](receive-folder-tables.md)を参照してください。 
  
実装、 **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) のプロパティのプロパティの制限の設定をサポートするためにフォルダーのテーブルを表示します。 このを有効に簡単にアクセスする特定のフォルダーが表示されます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDisplayReceiveFolderTable  <br/> |MFCMAPI では、 **IMsgStore::GetReceiveFolderTable**メソッドを使用して、表示する受信フォルダーのテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMsgStore: IMAPIProp](imsgstoreimapiprop.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

