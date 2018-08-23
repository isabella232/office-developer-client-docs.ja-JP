---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cc0039cf2210446704d25b2156bd4ff50041a524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586278"
---
# <a name="imapisessiongetmsgstorestable"></a>IMAPISession::GetMsgStoresTable

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
セッション ・ プロファイル内のすべてのメッセージ ・ ストアに関する情報を含むメッセージ ストアのテーブルへのアクセスを提供します。
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [in]文字の文字列の列の形式を決定するフラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> Unicode 形式では、文字列型の列です。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列型の列です。
    
 _lppTable_
  
> [out]メッセージ ストアのテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> テーブルが正常に返されました。
    
MAPI_E_BAD_CHARWIDTH 
  
> MAPI_UNICODE フラグが設定され、セッションが Unicode をサポートしていません。
    
## <a name="remarks"></a>注釈

**IMAPISession::GetMsgStoresTable**メソッドは、メッセージ ストアのテーブルへのポインターを取得、テーブルが管理している MAPI プロファイル内の各の開いているメッセージ ストアについての情報が含まれる。 
  
テーブルを格納、メッセージの必須およびオプションの列の一覧については、[メッセージ ストアのテーブル](message-store-tables.md)を参照してください。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

MAPI は、変更が発生するたびに、セッション中に、メッセージ ストアのテーブルを更新、ため **、メッセージ ストアのテーブルのこれらの変更の通知を登録するメソッド**を呼び出します。 行われた変更は、新しいメッセージ ストアの追加、削除、既存のストア、および、既定のストアに変更します。 
  
_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenMessageStoreTable  <br/> |MFCMAPI では、 **IMAPISession::GetMsgStoresTable**メソッドを使用して、MFCMAPI のメイン ダイアログ ボックスでレンダリングできるように、メッセージ ストアのテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[メッセージ ストア テーブル](message-store-tables.md)

