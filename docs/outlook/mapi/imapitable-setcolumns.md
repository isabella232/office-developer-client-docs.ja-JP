---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 45ac1cd1a55bc320aba5a725c26b964226fa1245
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600863"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルに列として表示するプロパティの特定のプロパティと順序を定義します。
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpPropTagArray_
  
> [in]テーブルに列として含めるプロパティを識別するプロパティ タグの配列へのポインター。 各タグのプロパティの種類の部分は、有効な型に設定するか、後続のPR_NULL領域を予約するために使用できます。 _lpPropTagArray_ パラメーターを NULL に設定することはできません。すべてのテーブルには、少なくとも 1 つの列が必要です。 
    
 _ulFlags_
  
> [in]通知で **SetColumns** を使用する場合など **、SetColumns** への非同期呼び出しの戻りを制御するフラグのビットマスク。 次のフラグを設定できます。 
    
TBL_ASYNC 
  
> 列設定操作を非同期的に実行して、操作が完全に完了する前に **SetColumns** が戻る可能性があるという要求。 
    
TBL_BATCH 
  
> データが実際に必要になるまで、テーブルが列設定操作を延期できます。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 列の設定操作が成功しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中で、列の設定操作が開始しなかっています。 進行中の操作の完了を許可するか、停止する必要があります。
    
## <a name="remarks"></a>注釈

テーブルの列セットは、テーブル内の行の列を表すプロパティのグループです。 テーブルの種類ごとに既定の列セットがあります。 既定の列セットは、テーブル実装者が自動的に含むプロパティで構成されます。 テーブル ユーザーは **、IMAPITable::SetColumns メソッドを呼び出すことによって、この既定のセットを変更** できます。 テーブルの実装者が列の削除をサポートしている場合、または列の順序を変更する場合は、他の列を既定のセットに追加する必要があります。 **SetColumns は** 、各行で返される列と、行内のこれらの列の順序を指定します。 
  
**SetColumns** 操作の成功は、テーブルのデータを取得するために後続の呼び出しが行われた後にのみ明らかです。 その後、エラーが報告されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

一部のプロバイダーでは **、SetColumns** 呼び出しを使用して、テーブル ビューで使用可能な列の一部であるテーブル列のみを順序付けできます。 他のプロバイダーでは **、SetColumns** 呼び出しを使用して、元の列セットに含まれるプロパティを含むすべてのテーブル列を並び替えできます。 
  
非同期TBL_BATCH設定されている場合、プロバイダーはプロパティの種類 PT_ERROR と、サポートされていない列のプロパティ値 NULL を返す必要があります。
  
操作を非同期に要求するTBL_ASYNCフラグに応答する必要はない。 非同期列セット定義をサポートしない場合は、同期的に操作を実行します。 このフラグをサポートして、TBL_ASYNC非同期操作がまだ進行中の場合は、このフラグをMAPI_E_BUSY。 それ以外の場合S_OK、プロパティ タグ配列に含まれるすべてのプロパティをサポートするかどうかに関係なく、値を返します。 サポートされていないプロパティに起因するエラーは **、QueryRows** などのデータを取得する IMAPITable メソッドから **返す必要があります**。 
  
Restrict の呼び出しによって表示されないテーブル行に対する通知を生成 **しません**。 
  
テーブル通知を送信する場合、TABLE_NOTIFICATION 構造体の行メンバー内のプロパティの順序と、最新の **SetColumns** 呼び出しで指定された順序は、通知要求が送信された時刻と同じにする必要があります。 [](table_notification.md) 
  
別のフラグTBL_BATCHを使用すると、呼び出し元は、テーブルの実装者が操作の結果の評価を後で延期できると指定できます。 可能な限り、バッチ処理された操作によってパフォーマンスが向上するために、呼び出し元はこのフラグを設定する必要があります。
  
多くの場合、呼び出し元は、取得した行セットの一部の列を予約して、後で値を追加する場合に便利です。 呼び出し元は、SetColumns に渡 **PR_NULLプロパティ** タグ配列内の目的の位置に [(PidTagNull)](pidtagnull-canonical-property.md)を配置して **、これを行います**。次に **、QueryRows** で **取得PR_NULL** 行の位置にテーブルが戻されます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpPropTagArray_ パラメーターのプロパティ タグ配列を作成する場合は、テーブル ビューに列を表示する順序でタグを並び替えます。 
  
複数値インスタンス フラグまたは定数をプロパティ タグに適用することで、列セットに含める複数値プロパティMVI_FLAG指定できます。 このフラグを設定するには、プロパティの単一値バージョンのプロパティ タグをパラメーターとして、MVI_PROPマクロに渡します。
  
```
MVI_PROP(ulPropTag)

```

プロパティMVI_PROPマクロMVI_FLAG設定し、タグを複数値タグに変換します。 1 つの値を持つプロパティMVI_PROP誤って呼び出しを試みた場合、MAPI は呼び出しを無視し、プロパティ タグを変更しません。 
  
プロパティ タグ配列にプロパティタグPR_NULLを含め、列セット内の領域を予約できます。 領域を予約すると、新しいプロパティ タグ配列を割り当てなくても列セットに追加できます。 
  
**SetColumns** の呼び出しによってテーブルの列の順序が変更され、これらの列の 1 つ以上が複数値プロパティを表す場合、テーブル内の行数が増える可能性があります。 この場合、テーブルのすべてのブックマークが破棄されます。 複数値の列がテーブルに与える影響の詳細については、「複数値列の操作 [」を参照してください](working-with-multivalued-columns.md)。
  
列の設定は、既定では同期操作です。 ただし、データが必要になるまで、テーブルで操作を延期するには、このフラグを設定TBL_BATCHできます。 このフラグを設定すると、パフォーマンスが向上します。 別のフラグTBL_ASYNC、操作を非同期にし、操作が完了する前に **SetColumns** を返します。 完了が発生した時刻を確認するには [、IMAPITable::GetStatus を呼び出します](imapitable-getstatus.md)。
  
**SetColumns** の呼び出しが MAPI_E_BUSY を返し、別の操作によって操作が開始されていないことを示す場合は [、IMAPITable::Abort](imapitable-abort.md)を呼び出して、進行中の操作を停止できます。 
  
また [、HrAddColumnsEx を呼び出して](hraddcolumnsex.md) 列セットを変更できます。 **HrAddColumnsEx** と **IMAPITable::SetColumns** の違いは **、HrAddColumnsEx** の柔軟性が低い点です。列の追加のみ可能です。 追加の列は、列セットの先頭に配置されます。すべての既存の列は、これらの列の後に表示されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::D oSetColumns  <br/> |MFCMAPI は **IMAPITable::SetColumns** メソッドを使用して、テーブルに必要な列を設定します。  <br/> |
   
## <a name="see-also"></a>関連項目



[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPITable::Abort](imapitable-abort.md)
  
[IMAPITable::GetRowCount](imapitable-getrowcount.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

