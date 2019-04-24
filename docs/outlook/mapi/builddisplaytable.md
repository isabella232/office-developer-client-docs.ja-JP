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
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318096"
---
# <a name="builddisplaytable"></a>BuildDisplayTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
1つ以上の[dtpage](dtpage.md)構造に含まれるプロパティページデータから、表示テーブルを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
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
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> 順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpmalloc_
  
> 使用NULL に設定する必要があります。 
    
 _hInstance_
  
> 順番**builddisplaytable**がリソースを取得する MAPI オブジェクトのインスタンス。 
    
 _cpages_
  
> 順番_lppage_パラメーターで指定された配列内の[dtpage](dtpage.md)構造体の数。 
    
 _lppage_
  
> 順番作成するテーブルの表示ページに関する情報を含む**dtpage**構造体の配列へのポインター。 
    
 _ulFlags_
  
> 順番フラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 渡された文字列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列は ANSI 形式になります。 
    
 _lpptable_
  
> 読み上げ表示テーブルへのポインターへのポインター。これには[IMAPITable](imapitableiunknown.md)インターフェイスが公開されます。 
    
 _lppTblData_
  
> [入力]_lpptable_パラメーターで返されるテーブルの[itabledata](itabledataiunknown.md)インターフェイスを公開するテーブルデータオブジェクトへのポインターへのポインター。 テーブルデータオブジェクトが必要ない場合は、ポインター値ではなく、 _lppTblData_を NULL に設定する必要があります。 
    
## <a name="return-value"></a>戻り値

なし
  
## <a name="remarks"></a>解説

MAPI では、特に、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、オブジェクトインターフェイスを呼び出すときに使用するメモリをクライアントアプリケーションに割り当てます。[imapiprop:: GetProps](imapiprop-getprops.md) and [IMAPITable:: QueryRows](imapitable-queryrows.md)など。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

考えられるすべての情報は、ダイアログリソースから読み取られます。次のようになります。
  
- ページのタイトル。これは、リソースのダイアログタイトルから読み取る[dtblpage](dtblpage.md)構造の_ulblpszlabel_メンバーです。 
    
- すべてのコントロールのタイトル。他のコントロール構造の_ulblpszlabel_メンバーは、リソースのコントロールテキストから読み取ります。 
    
 **builddisplaytable**は、入力制御構造で渡されたものをダイアログリソースからの情報で上書きします。これは、 **builddisplaytable**の呼び出し元がページまたはコントロールのタイトルを動的に指定できないことを意味します。 **builddisplaytable**を持つことができるようにする必要がある呼び出し元は、 _lppTableData_でテーブルデータオブジェクトを返し、その中の行を変更することができます。または、代わりにテーブルデータオブジェクトに手動で表示テーブルを作成することもできます。 
  
_lppTableData_が NULL に設定されていない場合、プロバイダーは、表示テーブルの操作が完了したときに、テーブルデータオブジェクトを解放することを担当します。 
  

