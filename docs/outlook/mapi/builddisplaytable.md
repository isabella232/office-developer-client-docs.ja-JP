---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c49d7176b74d2d6fafd3da0a4d658dd72c7b54c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621158"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1 つ以上の DTPAGE 構造に含まれるプロパティ ページ データから表示テーブル [を作成](dtpage.md) します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |サービス プロバイダー  <br/> |
   
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
  
> [in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。 
    
 _lpMalloc_
  
> 未使用。は NULL に設定する必要があります。 
    
 _hInstance_
  
> [in] **BuildDisplayTable** がリソースを取得する MAPI オブジェクトのインスタンス。 
    
 _cPages_
  
> [in]lpPage [パラメーターが指](dtpage.md) す配列内の  _DTPAGE 構造体の_ 数。 
    
 _lpPage_
  
> [in]作成する表示テーブル ページに関する情報を含む **DTPAGE** 構造体の配列へのポインター。 
    
 _ulFlags_
  
> [in]フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列は ANSI 形式になります。 
    
 _lppTable_
  
> [out] [IMAPITable](imapitableiunknown.md) インターフェイスを公開する表示テーブルへのポインターへのポインター。 
    
 _lppTblData_
  
> [in, out]_lppTable_ パラメーターで返されるテーブルの [ITableData](itabledataiunknown.md)インターフェイスを公開するテーブル データ オブジェクトへのポインター。 テーブル データ オブジェクトが必要ない場合は、ポインター値の代わりに  _lppTblData_ を NULL に設定する必要があります。 
    
## <a name="return-value"></a>戻り値

なし
  
## <a name="remarks"></a>注釈

MAPI では、ほとんどのメモリ割り当ておよび割り当て解除に _lpAllocateBuffer_ _、lpAllocateMore、lpFreeBuffer_ が指す関数を使用して、特に [IMAPIProp::GetProps](imapiprop-getprops.md)や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際にクライアント アプリケーションで使用するメモリを割り当てる。  
  
## <a name="notes-to-callers"></a>呼び出し側への注意

可能な限り、次のダイアログ リソースから読み取り可能です。
  
- [DTBLPAGE](dtblpage.md)構造の _ulbLpszLabel_ メンバーであるページ タイトルは、リソースのダイアログ タイトルから読み取ります。 
    
- リソース内のコントロール テキストから読み取った他のコントロール構造の  _ulbLpszLabel_ メンバーであるすべてのコントロール タイトル。 
    
 **BuildDisplayTable** は、ダイアログ リソースからの情報を使用して、入力コントロール構造で渡された内容を上書きします。 **つまり、BuildDisplayTable** の呼び出し元はページまたはコントロールのタイトルを動的に指定できません。 これを行う必要がある呼び出し元は **、BuildDisplayTable** が  _lppTableData_ のテーブル データ オブジェクトを返し、その中の行を変更できます。または、代わりにテーブル データ オブジェクトで表示テーブルを手で作成することもできます。 
  
_lppTableData が_ NULL に設定されていない場合、プロバイダーは、表示テーブルの終了時にテーブル データ オブジェクトを解放します。 
  

