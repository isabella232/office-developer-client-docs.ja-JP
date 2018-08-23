---
title: IMAPITableSetColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetColumns
api_type:
- COM
ms.assetid: 9a39cf8d-df0f-493c-b272-f15c65b3f15e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 9eeab1e1186aeb5a9b458facd59bd4cc155e8014
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800847"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**適用対象**: Outlook 
  
特定のプロパティと、テーブル内の列として表示するプロパティの順序を定義します。
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpPropTagArray_
  
> [in]テーブル内の列として含まれるプロパティを識別するプロパティ タグの配列へのポインター。 各タグのプロパティの型の部分は、以降の追加の領域を予約するのには有効な型または**PR_NULL**を設定できます。 _LpPropTagArray_パラメーターを null に設定できません。すべてのテーブルには、少なくとも 1 つの列が必要です。 
    
 _ulFlags_
  
> [in]**SetColumns**、 **SetColumns**が通知で使用する場合などの非同期の呼び出しの戻り値を制御するフラグのビットマスクです。 次のフラグを設定することができます。 
    
TBL_ASYNC 
  
> 列の設定操作の要求では、可能性のある操作が完全に終了する前に取得する**SetColumns**を非同期的に原因を実行します。 
    
TBL_BATCH 
  
> データが実際に必要になるまで、列の設定操作を延期するテーブルを許可します。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 列の設定の操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別進行中に、列の操作の開始を設定しないようにします。 実行中の操作を完了できるか、それを停止する必要があります。
    
## <a name="remarks"></a>注釈

テーブルの列のセットは、テーブル内の行の列を構成するプロパティのグループです。 テーブルの種類ごとに設定する既定の列があります。 自動的にテーブルの作成者を含むプロパティの既定の列セットが構成されています。 テーブルのユーザーには、この既定値は、 **IMAPITable::SetColumns**メソッドを呼び出すことによって設定を変更できます。 その他の列がテーブルの作成者はこれらの列を削除することや、列の順序を変更することをサポートしている場合は、設定の既定値に追加することを要求することができます。 **SetColumns**では、それぞれの行と行にこれらの列の順序で返される列を指定します。 
  
**SetColumns**操作の成功は、テーブルのデータを取得するために後続の呼び出しを実行した後にのみ明らかです。 エラーが報告されることですし。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

一部のプロバイダーは、テーブル ビューの使用可能な列の一部であるテーブルの列のみを注文する**SetColumns**呼び出しを許可します。 他のプロバイダーでは、 **SetColumns**呼び出し元の列のセットではなくプロパティが含まれているものも含めて、すべてのテーブルの列の順序を使用できます。 
  
非同期操作の TBL_BATCH を設定すると、プロバイダーは PT_ERROR のプロパティの種類とサポートされていない列の null プロパティの値を返す必要があります。
  
TBL_ASYNC フラグを要求する操作を非同期にすることに応答する必要はありません。 非同期の列のセットの定義をサポートしていない場合は、同期的に操作を実行します。 TBL_ASYNC のフラグは、別の非同期の操作をサポートできる場合、操作は、進行中、MAPI_E_BUSY の戻り値では。 それ以外の場合、すべてのプロパティ タグ配列に含まれているプロパティをサポートするかどうかに関係なく S_OK を返します。 **スプーラー**などのデータを取得する**IMAPITable**メソッドからエラーがサポートされていないプロパティの結果が返されます。 
  
**制限**を呼び出すことによってビューから非表示になっているテーブルの行への通知は生成されません。 
  
指定されたテーブルの通知、 [TABLE_NOTIFICATION](table_notification.md)構造体の**行**メンバーのプロパティの順序と順序を送信するときに最新の**SetColumns**呼び出し必要があります、通知を要求する時と同じ送信されました。 
  
別のフラグ、TBL_BATCH では、しばらくの間操作の結果を評価することができますテーブル実装側で遅延を指定する呼び出し元を許可します。 可能な限り、呼び出し元は、バッチ操作のパフォーマンスが向上するためにこのフラグを設定する必要があります。
  
呼び出し元が後で追加される値を取得した行セットの一部のカラムを予約する場合に便利なことがよくあります。 呼び出し元が**SetColumns**; に渡されるプロパティ タグ配列で、目的の位置に**PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) を配置することによってこれを行うテーブルは、**スプーラー**を返しますこれらのすべての行の位置に**PR_NULL**を取得し、されます。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_LpPropTagArray_パラメーターのプロパティ タグ配列を作成するときは、テーブル ビューに表示する列を希望する順序で、タグを注文します。 
  
プロパティ タグに複数値を持つインスタンスのフラグ、または MVI_FLAG の定数を適用することで設定する列に含まれる複数値を持つプロパティを指定できます。 単一値プロパティのバージョンのプロパティ タグ パラメーターとして渡し、MVI_PROP マクロを次のようにこのフラグを設定します。
  
```
MVI_PROP(ulPropTag)

```

MVI_PROP マクロは、プロパティは、複数値を持つタグにタグを有効にする MVI_FLAG を設定します。 誤っては、単一値プロパティに MVI_PROP を呼び出すと、MAPI 呼び出しを無視して、変更されていないプロパティ タグのままにします。 
  
プロパティ タグを**PR_NULL**に設定すると、列のセット内の領域を予約するプロパティ タグ配列を含めることができます。 領域を予約する、新しいプロパティ タグ配列を割り当てることがなく設定されている列を追加できます。 
  
**SetColumns**を呼び出すは、テーブルの列の順序変更し、1 つ以上のこれらの列は、複数値を持つプロパティを表す、増加するテーブル内の行の数のことができます。 このような場合は、テーブルのブックマークをすべて破棄されます。 方法の詳細については、複数値を持つ列はテーブルに影響を与える、[複数値を持つ列の使用](working-with-multivalued-columns.md)を参照してください。
  
列の設定は既定では同期操作です。 ただし、TBL_BATCH フラグを設定することによってデータが必要になるまで、操作を延期するテーブルを許可できます。 このフラグを設定すると、パフォーマンスが向上します。 別のフラグ、TBL_ASYNC によって操作が非同期操作が完了する前に戻るには、 **SetColumns**を許可します。 完了が発生した場合を確認するのには、 [IMAPITable::GetStatus](imapitable-getstatus.md)を呼び出します。
  
**SetColumns**呼び出しが別の操作が、操作の開始を拒否されていることを示す、MAPI_E_BUSY を返す場合は、実行中の操作を停止するのには[IMAPITable::Abort](imapitable-abort.md)を呼び出すことができます。 
  
列セットを変更するのには[HrAddColumnsEx](hraddcolumnsex.md)を呼び出すこともできます。 **HrAddColumnsEx**と**IMAPITable::SetColumns**の違いは、 **HrAddColumnsEx**が少ない柔軟性があります。列のみ追加できます。 追加の列は列セットの先頭に配置されます。これらの列の後にすべての既存の列が表示されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::DoSetColumns  <br/> |MFCMAPI では、 **IMAPITable::SetColumns**メソッドを使用して、目的のテーブルの列を設定します。  <br/> |
   
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

