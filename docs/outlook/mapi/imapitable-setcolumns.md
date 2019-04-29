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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 897330feb216dbc3ab143378977c77141cf488f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416350"
---
# <a name="imapitablesetcolumns"></a>IMAPITable::SetColumns

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
表に列として表示されるプロパティとプロパティの順序を定義します。
  
```cpp
HRESULT SetColumns(
LPSPropTagArray lpPropTagArray,
ULONG ulFlags
);
```

## <a name="parameters"></a>パラメーター

 _lpPropTagArray_
  
> 順番テーブル内の列として含めるプロパティを識別するプロパティタグの配列へのポインター。 各タグのプロパティの種類の部分は、有効な種類または**PR_NULL**に設定して、以降の追加のためにスペースを予約できます。 _lpPropTagArray_パラメーターを NULL に設定することはできません。各テーブルには、少なくとも1つの列が必要です。 
    
 _ulFlags_
  
> 順番**SetColumns**が通知で使用されている場合など、 **SetColumns**への非同期呼び出しの戻りを制御するフラグのビットマスク。 次のフラグを設定できます。 
    
TBL_ASYNC 
  
> 操作が完全に完了する前に**SetColumns**を戻すことができるように、列設定操作を非同期的に実行するように要求します。 
    
TBL_BATCH 
  
> テーブルで、データが実際に必要になるまで、列設定操作を延期できるようにします。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 列の設定操作が正常に完了しました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中であるため、列の設定操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
## <a name="remarks"></a>注釈

table の列セットは、テーブル内の行の列を構成するプロパティのグループです。 テーブルの種類ごとに既定の列セットがあります。 既定の列セットは、テーブルの作成者が自動的に含めるプロパティで構成されます。 Table ユーザーは、 **IMAPITable:: SetColumns**メソッドを呼び出すことによって、この既定のセットを変更できます。 これらのユーザーは、テーブルの実装で列が削除されるか、列の順序が変更される場合に、他の列が既定のセットに追加されるように要求できます。 **SetColumns**各行で返される列と、行内でこれらの列の順序を指定します。 
  
**SetColumns**操作の成功は、テーブルのデータを取得するために後続の呼び出しが行われた後にのみ、明らかです。 これにより、エラーが報告されます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

プロバイダーによっては、テーブルビューで使用可能な列の一部であるテーブル列のみを注文する**SetColumns**呼び出しを許可します。 その他のプロバイダーでは、 **SetColumns**呼び出しを使用して、元の列セットにないプロパティを含むすべてのテーブル列を並べ替えることができます。 
  
TBL_BATCH が非同期操作のために設定されている場合、プロバイダーは、サポートされていない列の PT_ERROR のプロパティの種類とプロパティの値を返す必要があります。
  
操作が非同期であることを要求する TBL_ASYNC フラグに応答する必要はありません。 非同期列セット定義をサポートしていない場合は、操作を同期的に実行します。 TBL_ASYNC フラグをサポートしていて、別の非同期操作がまだ実行中の場合は、MAPI_E_BUSY を返します。 それ以外の場合は、プロパティタグ配列に含まれるすべてのプロパティをサポートしているかどうかにかかわらず、S_OK を返します。 サポートされていないプロパティから生じるエラーは、 **QueryRows**などのデータを取得する**IMAPITable**メソッドから返されます。 
  
**制限**の呼び出しによって非表示になっているテーブルの行については通知を生成しません。 
  
テーブル通知を送信する場合、 [TABLE_NOTIFICATION](table_notification.md)構造体の**行**メンバーのプロパティと、最新の**SetColumns**呼び出しで指定されている順序は、通知要求の時刻と同じである必要があります。送信されました。 
  
もう1つのフラグ TBL_BATCH を使用すると、テーブルの実装者が後で操作の結果を評価することを指定できます。 バッチ処理を行うとパフォーマンスが向上するため、可能な限り、発信者はこのフラグを設定する必要があります。
  
後で値を追加するために、発信者が取得した行セットのいくつかの列を予約しておくと便利な場合がよくあります。 呼び出し元は、 **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)) を、 **SetColumns**に渡されたプロパティタグ配列内の目的の位置に配置することでこれを行います。その後、テーブルは**QueryRows**で取得されたすべての行のこれらの位置で**PR_NULL**を渡します。
  
## <a name="notes-to-callers"></a>呼び出し側への注意

_lpPropTagArray_パラメーターのプロパティタグの配列を作成するときは、テーブルビューに表示される列の順序でタグを並べ替えます。 
  
複数値のプロパティを指定するには、複数値のインスタンスのフラグ (MVI_FLAG 定数) を property タグに適用します。 このフラグを設定するには、プロパティの単一値バージョンのプロパティタグを、次のように MVI_PROP マクロのパラメーターとして渡します。
  
```
MVI_PROP(ulPropTag)

```

MVI_PROP マクロは、プロパティの MVI_FLAG を設定し、タグを複数値のタグに変換します。 単一値のプロパティで誤って MVI_PROP を呼び出そうとすると、MAPI は呼び出しを無視し、property タグを変更しないでおきます。 
  
プロパティタグの配列で**PR_NULL**に設定されているプロパティタグを、列セットにスペースを予約するように含めることができます。 スペースを予約すると、新しいプロパティタグ配列を割り当てずに、列セットを追加することができます。 
  
**SetColumns**の呼び出しによってテーブルの列の順序が変更され、これらの列の1つ以上が複数値プロパティを表している場合は、テーブル内の行数を増やすことができます。 この場合、テーブルのすべてのブックマークが破棄されます。 複数値列がテーブルにどのように影響するかの詳細については、「[複数値列の操作](working-with-multivalued-columns.md)」を参照してください。
  
既定では、列の設定は同期操作になります。 ただし、TBL_BATCH フラグを設定することによって、データが必要になるまで、テーブルが操作を延期できるようにすることができます。 このフラグを設定すると、パフォーマンスが向上します。 もう1つのフラグ TBL_ASYNC は、処理を非同期に行い、操作が完了する前に**SetColumns**を返すことができるようにします。 完了がいつ発生するかを確認するには、 [IMAPITable:: GetStatus](imapitable-getstatus.md)を呼び出します。
  
**SetColumns**の呼び出しによって MAPI_E_BUSY が返された場合は、別の操作によって操作を開始できないことを示します。 [IMAPITable:: Abort](imapitable-abort.md)を呼び出して、進行中の操作を停止することができます。 
  
[hraddcolumnsex](hraddcolumnsex.md)を呼び出して、列セットを変更することもできます。 **hraddcolumnsex**と**IMAPITable:: SetColumns**の違いは、 **hraddcolumnsex**の柔軟性が低いことです。列を追加することはできません。 追加の列は、列セットの先頭に配置されます。これらの列の下には、既存のすべての列が表示されます。 
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |CContentsTableListCtrl::D osetcolumns  <br/> |mfcmapi は、 **IMAPITable:: SetColumns**メソッドを使用して、テーブルに必要な列を設定します。  <br/> |
   
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

