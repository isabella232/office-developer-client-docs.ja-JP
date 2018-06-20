---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 7de404f421a405d80dd7f98beba5168969222fc9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800691"
---
# <a name="imapisessiongetstatustable"></a>IMAPISession::GetStatusTable

  
  
**適用されます**: Outlook 
  
ステータス テーブル、セッション内のすべての MAPI リソースに関する情報が含まれているテーブルへのアクセスを提供します。
  
```cpp
HRESULT GetStatusTable(
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
  
> [out]ステータス テーブルへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> テーブルが正常に返されました。
    
## <a name="remarks"></a>備考

**IMAPISession::GetStatusTable**メソッドは、セッション内のすべての MAPI リソースに関する情報を含むステータス テーブルへのアクセスを提供します。 MAPI サブシステムについての情報のテーブルの 1 行、1 行、MAPI スプーラーを無効、統合アドレス帳の 1 つの行とプロファイルには、各サービス プロバイダーの 1 つの行があります。 
  
状態テーブル内の必須および省略可能な列の一覧については、[ステータス ・ テーブル](status-tables.md)を参照してください。 
  
_UlFlags_パラメーターに MAPI_UNICODE フラグを設定する、 [IMAPITable::QueryColumns](imapitable-querycolumns.md)メソッドと[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは、 [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnStatusTable  <br/> |MFCMAPI では、 **IMAPISession::GetStatusTable**メソッドを使用してレンダリングされる状態のテーブルを取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[IMAPITable: IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPISession: IUnknown](imapisessioniunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)
  
[ステータス ・ テーブル](status-tables.md)

