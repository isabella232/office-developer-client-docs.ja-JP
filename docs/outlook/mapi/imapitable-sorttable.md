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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 46a87a6eb5c80244c04ae6257cd4441b8797ba36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800857"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**適用されます**: Outlook 
  
**IMAPITable::SortTable**メソッドは、条件の並べ替えによって、テーブルの行を指示します。 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

_lpSortCriteria_
  
> [in]適用する並べ替え条件を含む[SSortOrderSet](ssortorderset.md)構造体へのポインター。 0 の列を含む**SSortOrderSet**構造体を渡すと、特定の順序でソートするテーブルがないことを示します。 
    
_ulFlags_
  
> [in]**IMAPITable::SortTable**操作のタイミングを制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
TBL_ASYNC 
  
> 操作を非同期に開始し、操作が完了する前に返します。
    
TBL_BATCH 
  
> テーブル内のデータが必要になるまでは、並べ替えの完了を延期します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 並べ替え操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別の操作は、並べ替え操作の開始を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> テーブルは、要求の並べ替えの種類をサポートしていません。
    
MAPI_E_TOO_COMPLEX 
  
> テーブルは、 _lpSortCriteria_パラメーターで指定された特定の並べ替え条件が複雑すぎるために、操作を実行できません。 **SortTable**は、次の条件下で、MAPI_E_TOO_COMPLEX を返すことができます。 
    
   - 並べ替え操作がプロパティの列の要求された実装を並べ替えることはできません。
    
   - 実装は、 **ulOrder**の**SSortOrderSet**構造体のメンバーに要求された並べ替え順序をサポートしていません。 
    
   - 、ソートする列の数は**SSortOrderSet**で**cSorts**のメンバーで指定された、実装が処理できるよりも大きい。
    
   - **SSortOrderSet**、利用可能なまたはアクティブなセットに含まれていないプロパティに基づく内のプロパティ タグで示されるように、並べ替え操作が要求され、実装が利用可能なセットではなくプロパティの並べ替えをサポートしていません。
    
   - 1 つのプロパティが複数回指定されて、並べ替え順のセットで、同じプロパティ タグの複数のインスタンスによって示されると、実装は、このような並べ替え操作を実行できません。
    
   - MVI_FLAG を使用して複数値を持つプロパティの列に基づいて並べ替え操作が要求され、実装は、複数値を持つプロパティの並べ替えをサポートしていません。 
    
   - **SSortOrderSet**でのプロパティのプロパティ タグは、プロパティまたは実装でサポートされていない型を指定します。 
    
   - 以外の**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) は前方からのテーブルを処理する 1 つの並べ替え操作は、このような並べ替えをサポートしている添付ファイル テーブルに対してのみ指定されます。
    
## <a name="remarks"></a>備考

**IMAPITable::SortTable**メソッドでは、表形式ビューで行を順序付けします。 いくつかのテーブルでは、標準と分類の両方のさまざまな並べ替えのキー列の並べ替えをサポートするが、他のテーブルは多くのサポートに制限します。 通常、アドレス帳プロバイダーはテーブルの並べ替えをサポートしていません。 メッセージ ストア プロバイダーは、通常、(テーブル制限なし) の完全テーブルが並べ替えられたときに発生する、フォルダーの並べ替え順序を維持する並べ替えをサポートします。 
  
いくつかのテーブルでは、任意のテーブル列で実行する並べ替えを許可します。 他のテーブルの操作を行います。テーブル ビューに含まれていない列は、 **SortTable**の呼び出しによって影響を受けません。 いくつかのテーブルは、テーブルの現在の列セットの列にのみ並べ替えキーが作成されている必要があります。 
  
テーブルでは、並べ替え操作を完了できないことと、MAPI_E_NO_SUPPORT または MAPI_E_TOO_COMPLEX のいずれかを**SortTable**から返すことができます。 さらに、ストア プロバイダーは、階層テーブルの指定した並べ替え順を優先するとは限りません。 
  
_LpSortCriteria_パラメーターで指定された[SSortOrderSet](ssortorderset.md)構造体で 0 個の列がある場合、テーブルは、現在の列のセットを返します。 現在の並べ替え順序は、テーブルの[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)メソッドを呼び出すことによって取得できます。 
  
テーブルのすべてのブックマークは無効になり、 **SortTable**への呼び出しが作成され、テーブルの先頭に、現在のカーソル位置を示す BOOKMARK_CURRENT のブックマークを指定するときに削除する必要があります。 
  
MVI_FLAG フラグが設定されていない複数値を持つプロパティを含む列を並べ替える場合、列の値は、完全に順序付けられた組として扱われます。 2 つの複数値を持つ列の比較では、列の要素には、最初の非等値の列の関係を報告を比較し、比較対象の列には、同じ順序で同じ値が含まれている場合にのみ、等しいかどうかを返します。 もう一方よりも少ない値を 1 つの列には、報告された関係が他の値に null 値の
  
## <a name="notes-to-callers"></a>呼び出し側への注意

フラグのいずれかを設定しない限り、 **SortTable**は同期的に動作します。 **SortTable**に TBL_BATCH フラグを設定すると、データを要求する場合を除き、並べ替え操作を延期します。 TBL_ASYNC フラグが設定されている場合**SortTable**は、非同期的に、操作を完了する前に返す可能性があります。 
  
並べ替えをすぐに行う必要がある場合は、進行中の非同期操作を停止するのには[IMAPITable::Abort](imapitable-abort.md)メソッドを呼び出します。 **SortTable**は、テーブルの 1 つまたは複数の非同期操作が実行されているために続行できません、MAPI_E_BUSY が返されます。 
  
最適なパフォーマンスを得るには、テーブルの列のセットをカスタマイズする**SetColumns**と並べ替えを実行するのには**SortTable**を呼び出す前に、テーブル内の行の数を制限するため**だけに制限する**を呼び出します。 
  
**SortTable**が失敗したときに、問題が発生する前に有効であった並べ替え順序は、有効です。 
  
## <a name="see-also"></a>関連項目

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable: IUnknown](imapitableiunknown.md)

