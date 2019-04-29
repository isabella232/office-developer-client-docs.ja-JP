---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 26d6ffe66a5e7749c9d8c4e5210e9f72de808932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416294"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のカーソル位置から、1つまたは複数の行をテーブルから返します。
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>パラメーター

 _lrowcount_
  
> 順番返される行の最大数。
    
 _ulFlags_
  
> 順番行が返される方法を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TBL_NOADVANCE 
  
> 行の取得の結果として、カーソルが昇格しないようにします。 TBL_NOADVANCE フラグが設定されている場合、カーソルは返される最初の行を指します。 TBL_NOADVANCE フラグが設定されていない場合、カーソルは、返される最後の行の次の行を指します。
    
 _lpprows_
  
> 読み上げテーブルの行を保持する[srowset](srowset.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作が進行中なので、行取得操作を開始できません。 進行中の操作が完了することを許可するか、停止する必要があります。
    
MAPI_E_INVALID_PARAMETER 
  
> _irowcount_パラメーターは0に設定されています。 
    
## <a name="remarks"></a>注釈

**IMAPITable:: QueryRows**メソッドは、テーブルから1つまたは複数のデータ行を取得します。 _irowcount_パラメーターの値は、取得の開始点に影響します。 _irowcount_が正の場合は、現在の位置から順に行が読み取られます。 _irowcount_が負の場合、 **QueryRows**は指定された行数だけ後方に移動して開始点をリセットします。 カーソルがリセットされると、行は前方に読み上げられます。 
  
_lpprows_パラメーターが指す[srowset](srowset.md)構造の**cRows**メンバは、返される行数を示しています。 0行が返される場合: 
  
- カーソルは既にテーブルの先頭に配置されており、 _irowcount_の値が負になります。 や 
    
- カーソルは既にテーブルの最後に配置されており、 _irowcount_の値は正です。 
    
列の数とその順序は、各行で同じです。 行のプロパティが存在しない場合、またはプロパティの読み取りエラーが発生した場合、行内のプロパティの**spropvalue**構造体には次の値が含まれています。 
  
- **ulPropTag**メンバーのプロパティの種類の PT_ERROR。 
    
- **Value**メンバーの MAPI_E_NOT_FOUND。 
    
_lpprows_パラメーターによって指定された行セットの[spropvalue](spropvalue.md)構造体に使用されるメモリは、各行に対して個別に割り当てて解放する必要があります。 [MAPIFreeBuffer](mapifreebuffer.md)を使用して、プロパティの値構造を解放し、行セットを解放します。 **QueryRows**の呼び出しによって0が返されますが、テーブルの先頭または末尾を示している場合は、 **srowset**構造自体のみを解放する必要があります。 **srowset**構造のメモリを割り当てて解放する方法の詳細については、「 [adrlist および srowset 構造体のメモリの管理](managing-memory-for-adrlist-and-srowset-structures.md)」を参照してください。
  
返される行と、返される順序は、 [IMAPITable:: Restrict](imapitable-restrict.md)と[imapitable:: sorttable](imapitable-sorttable.md)に成功したかどうかによって異なります。 ビューからフィルター行を**制限**します。これにより、 **QueryRows**は、制限で指定された条件に一致する行のみを返します。 **sorttable**は、標準または分類された並べ替え順序を確立し、 **QueryRows**によって返される一連の行に影響します。 返される行は、 [ssortorderset](ssortorderset.md)構造で指定された順序で**sorttable**に渡されます。
  
各行に返される列と返される順序は、 [IMAPITable:: SetColumns](imapitable-setcolumns.md)に正常に呼び出しが行われたかどうかによって異なります。 **SetColumns**は列セットを確立し、テーブルの列に含めるプロパティと、それらを含める順序を指定します。 **SetColumns**呼び出しが行われている場合、各行の特定の列とそれらの列の順序は、呼び出しで指定された列セットと一致します。 **SetColumns**呼び出しが行われていない場合、テーブルは既定の列セットを返します。 
  
これらの呼び出しが行われていない場合、 **QueryRows**はテーブル内のすべての行を返します。 各行には、既定の順序で設定された既定の列が含まれています。 
  
[IMAPITable:: SetColumns](imapitable-setcolumns.md)の呼び出しで設定された列セットが PR_NULL に設定されている場合、 _lpprows_で返される行セット内の[spropvalue](spropvalue.md)配列には空のスロットが含まれます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

発信者は、サポートされていない列を列セットに含めることを要求できます。 この場合、PT_ERROR をプロパティタグのプロパティの種類部分に配置し、サポートされていない列のプロパティ値に MAPI_E_NOT_FOUND を設定します。 
  
行カウントは、要件ではなく要求として処理します。 クエリの方向に行がない場合は、要求された数になるまで、0行から任意の値を返すことができます。 
  
カテゴリ別のテーブルビューから行が要求されたときにユーザーに表示される行のみを返します。これにより、呼び出し元は、データの範囲に関する有効な前提条件を作成し、余分な作業を避けることができます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

通常は、 _lrowcount_パラメーターで指定した行数だけ行が入力されます。 ただし、メモリまたは実装の制限が問題になる場合や、処理がテーブルの先頭または末尾に達した後に発生した場合、 **QueryRows**は要求されたよりも少ない行数を返します。 
  
**QueryRows**が MAPI_E_BUSY を返す場合は、 [IMAPITable:: waitforcompletion](imapitable-waitforcompletion.md)メソッドを呼び出して、非同期操作が完了したときに**QueryRows**の呼び出しを再試行します。 
  
**QueryRows**を呼び出すときは、非同期通知のタイミングが原因で、 **QueryRows**から返される行セットが、基になるデータを正確に表示しない可能性があることに注意してください。 たとえば、メッセージを削除した後、それに対応する通知を受信する前に、フォルダーの contents テーブルに**QueryRows**を呼び出すと、削除された行が行セットに返されることになります。 ユーザーのデータの表示を更新する前に通知が到着するのを常に待機します。 
  
テーブルから行を取得する方法の詳細については、「[テーブルの行からデータを取得](retrieving-data-from-table-rows.md)する」を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl  <br/> |dwthreadの loadtable  <br/> |mfcmapi は、 **IMAPITable:: QueryRows**メソッドを使用して、ビューに読み込むテーブル内の行を取得します。  <br/> |
   
## <a name="see-also"></a>関連項目



[ADRENTRY](adrentry.md)
  
[FreeProws](freeprows.md)
  
[HrQueryAllRows](hrqueryallrows.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[SRowSet](srowset.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

