---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 3b5268f0b033126083a463f72e47c64957df07eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577689"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
プロパティ ページのデータが 1 つまたは複数の[DTPAGE](dtpage.md)構造体に含まれているから、表示された表を作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |サービス プロバイダー  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a>パラメーター

 _lpAllocateBuffer_
  
> [in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpMalloc_
  
> 未使用です。NULL に設定する必要があります。 
    
 _hInstance_
  
> [in]**BuildDisplayTable**リソースの取得元となる MAPI オブジェクトのインスタンス。 
    
 _cPages_
  
> [in]_LpPage_パラメーターが指す配列内の[DTPAGE](dtpage.md)構造体の数です。 
    
 _lpPage_
  
> [in]**DTPAGE**構造体を構築する、表示のテーブル ・ ページに関する情報を含む配列へのポインター。 
    
 _ulFlags_
  
> [in]フラグのビットマスクです。 次のフラグを設定することができます。
    
MAPI_UNICODE 
  
> 渡された文字列は、Unicode 形式では。 MAPI_UNICODE フラグが設定されていない場合は、ANSI 形式の文字列です。 
    
 _lppTable_
  
> [out][IMAPITable](imapitableiunknown.md)インターフェイスを公開する表示のテーブルへのポインターへのポインター。 
    
 _lppTblData_
  
> [で [チェック アウト]_LppTable_パラメーターで返されるテーブルの[ITableData](itabledataiunknown.md)インターフェイスを公開するテーブルのデータ オブジェクトへのポインターへのポインター。 テーブルのデータ オブジェクトが必要ない場合、ポインターの値ではなく、 _lppTblData_を NULL に設定する必要があります。 
    
## <a name="return-value"></a>戻り値

なし
  
## <a name="remarks"></a>注釈

MAPI が to で指された_lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと解放のための_lpFreeBuffer_具体的にはオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当て関数を使用してください。[IMAPIProp::GetProps](imapiprop-getprops.md) 、 [IMAPITable::QueryRows](imapitable-queryrows.md)などです。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

ダイアログ リソースから読み取り可能なすべてのものを含みます。
  
- ページのタイトルは、 _ulbLpszLabel_ 、 [DTBLPAGE](dtblpage.md)構造体のメンバー リソースのダイアログのタイトルから読み取る。 
    
- すべてのコントロールのタイトルは、リソース内のコントロールのテキストから読み取るその他の制御構造の_ulbLpszLabel_メンバー。 
    
 **BuildDisplayTable**は、 **BuildDisplayTable**の呼び出し側が動的にページまたはコントロールのタイトルを指定することはできませんが、ダイアログ リソースから情報を入力コントロールの構造体に渡されたものを上書きします。 呼び出し元を実行する必要がある**BuildDisplayTable**を持つことができる_lppTableData_で、テーブルのデータ オブジェクトを返すしでその行を変更します。または、ディスプレイ テーブル、テーブルのデータ オブジェクトに手動で構築されること代わりにことができます。 
  
_LppTableData_が NULL に設定されていない場合、プロバイダーは、表示された表の処理が終了すると、テーブルのデータ オブジェクトを解放することを担当します。 
  

