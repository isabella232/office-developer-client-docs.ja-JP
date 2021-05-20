---
title: IMAPITableSortTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SortTable
api_type:
- COM
ms.assetid: ff5f78ac-06cf-46fb-93da-5f4a3a5d1b22
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: f16ba9164d55fdb7bd688d4068f99dc4407e5413
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432367"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**適用対象**: Outlook 2013 | Outlook 2016 
  
**IMAPITable::SortTable** メソッドは、並べ替え条件に応じて、テーブルの行を順序付けします。 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

_lpSortCriteria_
  
> [in]適用する並べ替え条件を含む [SSortOrderSet](ssortorderset.md) 構造体へのポインター。 0 **列を含む SSortOrderSet** 構造体を渡す場合は、テーブルを特定の順序で並べ替える必要が無い場合を示します。 
    
_ulFlags_
  
> [in] **IMAPITable::SortTable** 操作のタイミングを制御するフラグのビットマスク。 次のフラグを設定できます。 
    
TBL_ASYNC 
  
> 操作を非同期的に開始し、操作が完了する前に返します。
    
TBL_BATCH 
  
> テーブル内のデータが必要になるまで、並べ替えの完了を延期します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 並べ替え操作が成功しました。
    
MAPI_E_BUSY 
  
> 並べ替え操作の開始を妨げる別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> テーブルは、要求された並べ替えの種類をサポートしていない。
    
MAPI_E_TOO_COMPLEX 
  
> _lpSortCriteria_ パラメーターが指す特定の並べ替え条件が複雑すぎるため、テーブルは操作を実行できません。 **SortTable は** 、次のMAPI_E_TOO_COMPLEXの値を返します。 
    
   - 実装で並べ替えできないプロパティ列の並べ替え操作が要求されます。
    
   - 実装では **、SSortOrderSet** 構造体の **ulOrder** メンバーで要求された並べ替え順序はサポートされていません。 
    
   - **SSortOrderSet** の **cSorts** メンバーで指定されている並べ替える列の数は、実装で処理できる列よりも大きくなります。
    
   - **SSortOrderSet** のプロパティ タグで示される並べ替え操作は、使用可能なセットまたはアクティブなセットに含けられていないプロパティに基づいて要求され、実装では、使用可能なセット内に存在しないプロパティの並べ替えをサポートしていない。
    
   - 1 つのプロパティは、同じプロパティ タグの複数のインスタンスで示される並べ替え順序セットで複数回指定され、実装ではこのような並べ替え操作を実行できません。
    
   - 複数値プロパティ列に基づく並べ替え操作は、MVI_FLAG を使用して要求され、実装では複数値プロパティの並べ替えをサポートされていません。 
    
   - **SSortOrderSet** のプロパティのプロパティ タグは、実装がサポートしていないプロパティまたは型を指定します。 
    
   - **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティからテーブルを順方向に移動する並べ替え操作以外の並べ替え操作は、この種類の並べ替えをサポートする添付ファイル テーブルにのみ指定されます。
    
## <a name="remarks"></a>注釈

**IMAPITable::SortTable** メソッドは、テーブル ビュー内の行を並べ替えます。 一部のテーブルでは、さまざまな並べ替えキー列での標準並べ替えと分類された並べ替えの両方がサポートされている一方で、他のテーブルではサポートが制限されています。 通常、アドレス帳プロバイダーはテーブルの並べ替えをサポートしていない。 メッセージ ストア プロバイダーは、通常、完全なテーブル (制限のないテーブル) を並べ替えたときに結果のフォルダーの並べ替え順序を維持する範囲で並べ替えをサポートします。 
  
一部のテーブルでは、任意のテーブル列で並べ替えを実行できます。 他のテーブルは使用できません。テーブル ビューに含まれていない列は、SortTable 呼び出し **の影響を受** けません。 一部のテーブルでは、テーブルの現在の列セット内の列でのみ並べ替えキーを作成する必要があります。 
  
並べ替え操作をMAPI_E_NO_SUPPORTできない **MAPI_E_TOO_COMPLEX、SortTable** からテーブルを返す場合があります。 さらに、ストア プロバイダーは、階層テーブルに指定された並べ替え順序セットを尊重する保証はありません。 
  
_lpSortCriteria_ パラメーターが指す [SSortOrderSet](ssortorderset.md)構造体に列が 0 の場合、テーブルは現在の列セットを返します。 現在の並べ替え順序は、テーブルの [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドを呼び出すことによって取得できます。 
  
テーブルのすべてのブックマークは無効化され **、SortTable** の呼び出しが行われたときに削除され、現在のカーソル位置を示す BOOKMARK_CURRENT ブックマークをテーブルの先頭に設定する必要があります。 
  
MVI_FLAG フラグを設定せずに複数値プロパティを含む列で並べ替える場合、列の値は完全に順序付けられた組として扱います。 2 つの複数値列の比較では、列要素を順番に比較し、列の関係を最初の不等式で報告し、比較対象の列に同じ値が同じ順序で含まれている場合にのみ等値を返します。 1 つの列の値が他の列よりも少ない場合、報告される関係は、もう一方の値に対する null 値の関係になります。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フラグのいずれかを設定しない限り **、SortTable** は同期的に動作します。 このフラグを設定TBL_BATCH、データを要求しない限り **、SortTable** は並べ替え操作を延期します。 このフラグTBL_ASYNC設定すると **、SortTable** は非同期的に動作し、操作が完了する前に戻る可能性があります。 
  
並べ替えを直ちに行う必要がある場合は [、IMAPITable::Abort](imapitable-abort.md) メソッドを呼び出して、進行中の非同期操作を停止します。 テーブル **に対する 1** つ以上の非同期操作が進行中のため、SortTable を続行できない場合は、テーブルのMAPI_E_BUSY。 
  
最適なパフォーマンスを得る場合は **、SetColumns** を呼び出してテーブルの列セットをカスタマイズし、並べ替えを実行するために **SortTable** を呼び出す前に、テーブル内の行数を制限します。 
  
**SortTable が失敗** するたびに、エラーが発生する前に有効だった並べ替え順序は引き続き有効です。 
  
## <a name="see-also"></a>関連項目

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

