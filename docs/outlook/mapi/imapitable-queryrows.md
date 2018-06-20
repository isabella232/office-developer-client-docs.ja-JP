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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: a6659f64f6e8d2e3dc61819b2263efe672cdd15c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800865"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**適用されます**: Outlook 
  
現在のカーソル位置から開始し、テーブルから 1 つまたは複数の行を返します。
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>Parameters

 _lRowCount_
  
> [in]返される行の最大数。
    
 _ulFlags_
  
> [in]行を返す方法を制御するフラグのビットマスクです。 次のフラグを設定することができます。
    
TBL_NOADVANCE 
  
> カーソルが行の取得の結果として進化するを防ぎます。 TBL_NOADVANCE フラグが設定されている場合、カーソルが指す最初の行が返されます。 TBL_NOADVANCE フラグが設定されていない場合、カーソルは、返された最後の行を次の行をポイントします。
    
 _lppRows_
  
> [out]テーブルの行を保持している[SRowSet](srowset.md)構造体へのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> 行は正常に返されました。
    
MAPI_E_BUSY 
  
> 別の操作は、行の取得操作の開始を防止する処理中です。 実行中の操作を完了できるか、それを停止する必要があります。
    
MAPI_E_INVALID_PARAMETER 
  
> _IRowCount_パラメーターは、0 に設定されています。 
    
## <a name="remarks"></a>備考

**IMAPITable::QueryRows**メソッドは、テーブルから 1 つまたは複数行のデータを取得します。 _IRowCount_パラメーターの値は、検索の開始点に影響します。 _IRowCount_が正の場合は、現在位置から前方に行が読み取られます。 _IRowCount_が負の場合は、**スプーラー**は、指定された行の数を逆方向に移動開始点をリセットします。 カーソルをリセットした後は、前方の順序で行が読み取られます。 
  
[SRowSet](srowset.md)構造体を_lppRows_パラメーターが指す**カラス**のメンバーでは、返される行の数を示します。 場合は 0 個の行が返されます。 
  
- テーブルの先頭にカーソルが位置し、 _IRowCount_の値が負の値です。 - または - 
    
- テーブルの末尾にカーソルが既に配置されているし、 _IRowCount_の値が正の数値です。 
    
列とその順序の数は、行ごとに同じです。 行のプロパティが存在しません、またはプロパティを読み取り中にエラーがありますが、行のプロパティに [ **SPropValue**構造体には、次の値が含まれています。 
  
- **UlPropTag**メンバーのプロパティの型の PT_ERROR。 
    
- **値**メンバーの MAPI_E_NOT_FOUND。 
    
_LppRows_パラメーターで指定された行セット内の[SPropValue](spropvalue.md)構造体に使用されるメモリ必要があります個別に割り当てられ、行ごとに解放します。 [MAPIFreeBuffer](mapifreebuffer.md)を使用して、プロパティ値の構造体を解放して行を解放するために設定します。 **スプーラー**への呼び出しでは、0 を返す、ただし、先頭または末尾の表に示す**SRowSet**構造のみ必要がありますが解放されます。 割り当ておよび**SRowSet**構造体にメモリを解放する方法の詳細については、 [ADRLIST および SRowSet 構造体のメモリを管理する](managing-memory-for-adrlist-and-srowset-structures.md)を参照してください。
  
返される行とは、返される順序は、かどうか成功した呼び出しに加えられた[IMAPITable::Restrict](imapitable-restrict.md)および[IMAPITable::SortTable](imapitable-sorttable.md)によって異なります。 **制限**は、制限で指定された条件に一致する行だけを返すには、**スプーラー**の原因と、ビューから行をフィルター処理します。 **SortTable**は、標準を確立または**スプーラー**によって返される行の順序に影響を与えず、並べ替え順序を分類します。 **SortTable**に渡された[SSortOrderSet](ssortorderset.md)の構造体で指定された順序では、返される行です。
  
行ごとに列が返されに[IMAPITable::SetColumns](imapitable-setcolumns.md)するかどうかの正常な呼び出しがありましたが返される順序に依存しています。 **SetColumns**では、テーブルと、それらを含めるように順序の列に含まれるプロパティを指定する、列のセットを確立します。 **SetColumns**呼び出しを行った場合それぞれの行と列の順序で特定の列の設定の呼び出しで指定した列と同じです。 **SetColumns**呼び出しが作成されなかった場合、テーブルは、既定の列セットを返します。 
  
なしのこれらの呼び出しを行った場合は、**スプーラー**はテーブルのすべての行を返します。 各行には、既定の順序で設定する既定の列が含まれています。 
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)への呼び出しで確立された列のセットには、PR_NULL に設定された列が含まれている_lppRows_で返される行セット内で[SPropValue](spropvalue.md)配列に空のスロットが含まれます。 
  
## <a name="notes-to-implementers"></a>実装者へのメモ

列セットに含まれる、サポートされていない列を要求する呼び出し元を許可できます。 この問題が発生したときは、サポートされていない列のプロパティの値のプロパティ タグは MAPI_E_NOT_FOUND のプロパティの型の部分で PT_ERROR を配置します。 
  
要件ではなく、要求には、ローの数を処理します。 返品できます任意の場所から 0 個の行では、要求数、クエリの方向に行がない場合。 
  
ユーザーに表示される行を分類した表のビューでは、要求時にデータの範囲について、有効な判断を行うし、余分な作業を避けるために呼び出し元を許可する行のみを返します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

通常は最終的に、 _lRowCount_パラメーターで指定した数の行です。 ただし、メモリまたは実装の制限が問題である場合、または操作に達すると、テーブルの前後処理の途中では、**スプーラー**は要求されたよりも行数が少ないを返します。 
  
**スプーラー**では、MAPI_E_BUSY が返された場合は、 [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)メソッドを呼び出すし、非同期操作が完了すると、**スプーラー**への呼び出しを再試行してください。 
  
**スプーラー**を呼び出すときは、非同期通知のタイミングになる戻る**スプーラー**から基になるデータを正確に表現する行セットを引き起こす可能性ことに注意します。 たとえば、メッセージが対応する通知の受信前に削除する削除された行の行に返されると、フォルダーの内容の表の次に**スプーラー**に呼び出しを設定します。 常に通知データのユーザーのビューを更新する前に到着するまで待機します。 
  
テーブルから行を取得する方法の詳細については、[テーブルの行からのデータの取得](retrieving-data-from-table-rows.md)を参照してください。
  
## <a name="mfcmapi-reference"></a>MFCMAPI 参照

MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B
  
|**�t�@�C��**|**�֐�**|**�R�����g**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI では、 **IMAPITable::QueryRows**メソッドを使用して、ビューにロードするテーブル内の行を取得します。  <br/> |
   
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
  
[IMAPITable: IUnknown](imapitableiunknown.md)


[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)

