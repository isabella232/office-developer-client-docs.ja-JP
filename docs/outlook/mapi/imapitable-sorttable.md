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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328855"
---
# <a name="imapitablesorttable"></a>IMAPITable::SortTable

**適用対象**: Outlook 2013 | Outlook 2016 
  
**IMAPITable:: sorttable**メソッドは、並べ替え条件に従って、テーブルの行を順序付けることができます。 
  
```cpp
HRESULT SortTable(
LPSSortOrderSet lpSortCriteria,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

_lpsortcriteria_
  
> 順番適用する並べ替え基準を含む[ssortorderset](ssortorderset.md)構造体へのポインター。 列が0の**ssortorderset**構造を渡すと、テーブルを特定の順序で並べ替える必要がないことを示します。 
    
_ulFlags_
  
> 順番**IMAPITable:: sorttable**操作のタイミングを制御するフラグのビットマスク。 次のフラグを設定できます。 
    
TBL_ASYNC 
  
> 操作を非同期的に開始し、操作が完了する前に制御を戻します。
    
TBL_BATCH 
  
> テーブル内のデータが必要になるまで、並べ替えの完了を延期します。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 並べ替え操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中なので、並べ替え操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
MAPI_E_NO_SUPPORT 
  
> テーブルは、要求された並べ替えの種類をサポートしていません。
    
MAPI_E_TOO_COMPLEX 
  
> _lpsortcriteria_パラメーターによって指定された特定の並べ替え条件が複雑すぎるため、テーブルが操作を実行できません。 **sorttable**は、次の条件下で MAPI_E_TOO_COMPLEX を返すことができます。 
    
   - 実装で並べ替えることができないプロパティ列に対して並べ替え操作が要求されています。
    
   - 実装では、 **ssortorderset**構造の**ulorder**メンバーで要求されている並べ替え順序はサポートされていません。 
    
   - **ssortorderset**の csorts メンバーで指定され**** ているように並べ替えられる列の数が、実装で処理できるサイズを超えています。
    
   - 使用可能なセットまたはアクティブなセットに含まれていないプロパティに基づいて、 **ssortorderset**のプロパティタグによって示されているように、並べ替え操作が要求されます。実装は、使用可能なセットに含まれていないプロパティに対する並べ替えをサポートしていません。
    
   - 1つのプロパティが、同じプロパティタグの複数のインスタンスによって示されるように、並べ替え順序セットで複数回指定されています。実装では、このような並べ替え操作を実行できません。
    
   - 複数値プロパティ列に基づく並べ替え操作は、MVI_FLAG を使用して要求されます。実装では、複数値プロパティの並べ替えはサポートされていません。 
    
   - **ssortorderset**のプロパティのプロパティタグには、実装でサポートされていないプロパティまたは型が指定されています。 
    
   - **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) プロパティの前にあるテーブルを処理する以外の並べ替え操作は、この種類の並べ替えをサポートする添付ファイルテーブルに対してのみ指定されます。
    
## <a name="remarks"></a>解説

**IMAPITable:: sorttable**メソッドは、テーブルビュー内の行の順序を示します。 一部の表では、さまざまな並べ替えキー列に対して標準の並べ替えと分類された並べ替えの両方をサポートしています。 アドレス帳プロバイダーは、通常、テーブルの並べ替えをサポートしていません。 通常、メッセージストアプロバイダーは、完全なテーブル (制限なしのテーブル) が並べ替えられている場合に、結果となるフォルダーの並べ替え順序を維持することによって、エクステントへの並べ替えをサポートしています。 
  
テーブルによっては、任意の表の列に対して並べ替えを実行することができます。 その他のテーブルは含まれません。テーブルビューに含まれていない列は、 **sorttable**呼び出しの影響を受けません。 一部のテーブルでは、テーブルの現在の列セットの列を指定して並べ替えキーを作成する必要があります。 
  
表は、並べ替え操作を完了できない**** 場合に、MAPI_E_NO_SUPPORT または MAPI_E_TOO_COMPLEX のいずれかを返すことができます。 さらに、ストアプロバイダーは、階層テーブルに指定された並べ替え順序セットを優先することを保証されません。 
  
_lpsortcriteria_パラメーターで指定された[ssortorderset](ssortorderset.md)構造体に0列がある場合、テーブルは現在の列セットを返します。 現在の並べ替え順序を取得するには、テーブルの[IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドを呼び出します。 
  
テーブルのすべてのブックマークは無効になっており、 **sorttable**への呼び出しが行われ、現在のカーソル位置を示す BOOKMARK_CURRENT ブックマークがテーブルの先頭に設定されている必要があります。 
  
MVI_FLAG フラグが設定されていない複数値プロパティを含む列に対して並べ替えを行う場合、列の値は完全に順序付けられた組として扱われます。 2つの複数値列の比較によって、列の要素が順に比較され、最初の不等式の列のリレーションシップがレポートされます。比較する列に同じ順序で同じ値が含まれている場合にのみ、等価を返します。 一方の列の値がもう一方の列の値よりも小さい場合は、レポートされたリレーションシップは、null 値が他の値になることを示します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

**sorttable**は、フラグの1つを設定しない限り、同期して動作します。 TBL_BATCH フラグを設定すると、データを要求しない限り、 **sorttable**は並べ替え操作を延期します。 TBL_ASYNC フラグが設定されている場合、 **sorttable**は非同期で動作し、操作が完了する前に戻る可能性があります。 
  
必要な処理を停止するには、 [IMAPITable:: Abort](imapitable-abort.md)メソッドを呼び出します。並べ替えをすぐに実行する必要がある場合です。 テーブルに対する1つ以上の非同期操作が進行中であるために**sorttable**を続行できない場合は、MAPI_E_BUSY が返されます。 
  
最適なパフォーマンスを得るために、 **SetColumns**を呼び出してテーブルの列セットをカスタマイズし、並べ替えを実行する前にテーブル**** の行数を制限するように**制限**します。 
  
**sorttable**に障害が発生すると、その前に有効になっていた並べ替え順序が引き続き有効になります。 
  
## <a name="see-also"></a>関連項目

- [IMAPITable::Abort](imapitable-abort.md)
- [IMAPITable::GetRowCount](imapitable-getrowcount.md)
- [IMAPITable::QueryColumns](imapitable-querycolumns.md)
- [IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
- [IMAPITable::SetColumns](imapitable-setcolumns.md)
- [SSortOrderSet](ssortorderset.md)
- [IMAPITable : IUnknown](imapitableiunknown.md)

