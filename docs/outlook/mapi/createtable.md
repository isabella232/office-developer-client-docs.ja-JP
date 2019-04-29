---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435013"
---
# <a name="createtable"></a>CreateTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブルの内容を作成するために使用できる[itabledata](itabledataiunknown.md)オブジェクトの構造とオブジェクトハンドルを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a>パラメーター

 _lpinterface_
  
> 順番テーブルデータオブジェクトのインターフェイス識別子 (IID) へのポインター。 有効なインターフェイス識別子は IID_IMAPITableData です。 _lpinterface_パラメーターで NULL を渡すと、 _lppTableData_パラメーターで返されるテーブルデータオブジェクトも、テーブルデータオブジェクトの標準インターフェイスにキャストされます。 
    
 _lpAllocateBuffer_
  
> 順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> 順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpfreebuffer_
  
> 順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpvreserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _ulTableType_
  
> 順番クライアントアプリケーションまたはサービスプロバイダーが[IMAPITable:: GetStatus](imapitable-getstatus.md)の一部として使用できるテーブルの種類。テーブルビューにデータを返します。 使用可能な値は次のいずれかです。 
    
TBLTYPE_DYNAMIC 
  
> テーブルの内容は動的であり、基になるデータの変更に応じて変更できます。 
    
TBLTYPE_KEYSET 
  
> 表の行は固定されていますが、これらの行の値は動的であり、基になるデータの変更として変更されることがあります。 
    
TBLTYPE_SNAPSHOT 
  
> テーブルは静的であり、基になるデータが変更されても内容は変わりません。 
    
 _ulPropTagIndexColumn_
  
> 順番テーブルデータを変更するときに使用する列のインデックス番号を指定します。 
    
 _lpSPropTagArrayColumns_
  
> 順番オブジェクトがデータを保持するテーブルで必要なプロパティを示す、プロパティタグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
 _lppTableData_
  
> 読み上げ返されるテーブルデータオブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

_lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_の入力パラメーターは、それぞれ、 [MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)関数を指しています。 **CreateTable**を呼び出すクライアントアプリケーションは、という名前の MAPI 関数へのポインターを渡します。サービスプロバイダーは、初期化呼び出しで受け取った、または[imapiallocルーチン](imapisupport-getmemallocroutines.md)メソッドへの呼び出しによって取得したこれらの関数にポインターを渡します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)

