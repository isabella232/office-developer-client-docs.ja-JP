---
title: IMAPITableQueryRows
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.QueryRows
api_type:
- COM
ms.assetid: f26384f1-467e-4343-92b3-0425da9d2123
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f21172c00f1b5130de657e7018d05f04d16afe5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625351"
---
# <a name="imapitablequeryrows"></a>IMAPITable::QueryRows

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
現在のカーソル位置から始まる、テーブルから 1 つ以上の行を返します。
  
```cpp
HRESULT QueryRows(
LONG lRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows
);
```

## <a name="parameters"></a>パラメーター

 _lRowCount_
  
> [in]返される行の最大数。
    
 _ulFlags_
  
> [in]行の返し方を制御するフラグのビットマスク。 次のフラグを設定できます。
    
TBL_NOADVANCE 
  
> 行の取得の結果としてカーソルが進むのを防ぐ。 このフラグTBL_NOADVANCE設定すると、カーソルは返される最初の行をポイントします。 このフラグTBL_NOADVANCE設定されていない場合、カーソルは最後に返された行の後の行をポイントします。
    
 _lppRows_
  
> [out]テーブルの行を保持する [SRowSet](srowset.md) 構造体へのポインターを指すポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 行が正常に返されました。
    
MAPI_E_BUSY 
  
> 行の取得操作が開始されるのを防ぐ別の操作が進行中です。 進行中の操作の完了を許可するか、停止する必要があります。
    
MAPI_E_INVALID_PARAMETER 
  
> _IRowCount パラメーター_ は 0 に設定されます。 
    
## <a name="remarks"></a>注釈

**IMAPITable::QueryRows** メソッドは、テーブルから 1 行以上のデータを取得します。 _IRowCount パラメーターの値_ は、取得の開始点に影響します。 _IRowCount が正_ の場合、行は現在の位置から順方向に読み取ります。 _IRowCount が_ 負の場合 **、QueryRows は** 指定された行数を後方に移動して開始点をリセットします。 カーソルがリセットされた後、行は順方向に読み取りされます。 
  
**lppRows** パラメーターが指す [SRowSet](srowset.md)構造体の _cRows_ メンバーは、返される行数を示します。 0 行が返される場合は、次の処理を行います。 
  
- カーソルはテーブルの先頭に既に配置され  _、IRowCount_ の値は負の値です。 -Or- 
    
- カーソルはテーブルの末尾に既に配置され  _、IRowCount_ の値は正の値です。 
    
列の数とその順序は、各行で同じです。 行に対してプロパティが存在しない場合、またはプロパティの読み取りエラーが発生した場合、行のプロパティ **の SPropValue** 構造体には、次の値が含まれます。 
  
- PT_ERRORのプロパティの種類を **指定** します。 
    
- MAPI_E_NOT_FOUNDメンバー **の値を指定** します。 
    
_lppRows_ パラメーターが指す行セット内の [SPropValue](spropvalue.md)構造体に使用されるメモリは、行ごとに個別に割り当て、解放する必要があります。 [MAPIFreeBuffer を使用して](mapifreebuffer.md)、プロパティ値構造を解放し、行セットを解放します。 **ただし、QueryRows** の呼び出しが 0 を返す場合、テーブルの先頭または末尾を示す場合は **、SRowSet** 構造体自体のみを解放する必要があります。 SRowSet 構造体でメモリを割り当て、解放する方法の詳細については [、「ADRLIST](managing-memory-for-adrlist-and-srowset-structures.md)および **SRowSet** 構造体のメモリの管理」を参照してください。
  
返される行と、返される順序は [、IMAPITable::Restrict](imapitable-restrict.md) と [IMAPITable::SortTable](imapitable-sorttable.md)に対して正常に呼び出されたかどうかによって異なされます。 **ビュー** からフィルター行を制限すると **、QueryRows** は制限で指定された条件に一致する行のみを返します。 **SortTable は** 、標準または分類された並べ替え順序を確立し **、QueryRows** によって返される行のシーケンスに影響します。 返される行は **、SortTable** に渡される [SSortOrderSet](ssortorderset.md)構造体で指定された順序です。
  
各行に対して返される列と、返される順序は [、IMAPITable::SetColumns](imapitable-setcolumns.md)に対して正常に呼び出されたかどうかによって異なる。 **SetColumns は** 列セットを確立し、テーブル内の列に含めるプロパティと、その列を含める順序を指定します。 **SetColumns 呼** び出しが行われた場合、各行の特定の列とそれらの列の順序は、呼び出しで指定された列セットと一致します。 **SetColumns 呼び出し** が行われた場合、テーブルは既定の列セットを返します。 
  
これらの呼び出しが行われた場合 **、QueryRows は** テーブル内のすべての行を返します。 各行には、既定の列セットが既定の順序で含まれる。 
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)への呼び出しで確立された列セットに PR_NULL に設定された列が含まれている場合 _、lppRows_ で返される行セット内の [SPropValue](spropvalue.md)配列には空のスロットが含まれます。 
  
## <a name="notes-to-implementers"></a>実装に関するメモ

呼び出し元が、サポートされていない列を列セットに含める要求を許可できます。 この場合は、プロパティ PT_ERRORのプロパティの種類の部分に配置し、サポートされていない列MAPI_E_NOT_FOUNDプロパティ値に配置します。 
  
行数は、要件ではなく要求として扱います。 クエリの方向に行がない場合は、ゼロ行から要求された数まで任意の場所を返します。 
  
分類されたテーブル ビューから行が要求された場合に表示される行のみを返し、呼び出し元はデータの範囲に関する有効な仮定を行い、余分な作業を回避できます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

通常  _、lRowCount_ パラメーターで指定した数の行が表示されます。 ただし、メモリまたは実装の制限が問題である場合、または操作がテーブルの開始または終了に途中で達すると **、QueryRows** は要求された行よりも少ない行を返します。 
  
**QueryRows が** MAPI_E_BUSYを返す場合は [、IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)メソッドを呼び出し、非同期操作が完了したら **QueryRows** への呼び出しを再試行します。 
  
**QueryRows** を呼び出す場合、非同期通知のタイミングによって **、QueryRows** から取得した行セットが基になるデータを正確に表していない可能性があります。 たとえば、メッセージを削除した後で、対応する通知を受信する前にフォルダーのコンテンツ テーブルに **QueryRows** を呼び出した場合、削除された行が行セットで返されます。 ユーザーのデータビューを更新する前に、通知が届くのを常に待ちます。 
  
テーブルから行を取得する方法の詳細については、「 [テーブルの行からデータを取得する」を参照してください](retrieving-data-from-table-rows.md)。
  
## <a name="mfcmapi-reference"></a>MFCMAPI リファレンス

MFCMAPI のサンプル コードについては、次の表を参照してください。
  
|**ファイル**|**関数**|**コメント**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI は **IMAPITable::QueryRows** メソッドを使用して、ビューに読み込むテーブル内の行を取得します。  <br/> |
   
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

