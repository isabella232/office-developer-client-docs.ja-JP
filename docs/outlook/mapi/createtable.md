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
  
テーブルの内容を作成するために使用できる [ITableData](itabledataiunknown.md) オブジェクトの構造とオブジェクト ハンドルを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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

 _lpInterface_
  
> [in]テーブル データ オブジェクトのインターフェイス識別子 (IID) へのポインター。 有効なインターフェイス識別子はIID_IMAPITableData。 _lpInterface_ パラメーターに NULL を渡すと _、lppTableData_ パラメーターで返されるテーブル データ オブジェクトがテーブル データ オブジェクトの標準インターフェイスにキャストされます。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。 
    
 _lpvReserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _ulTableType_
  
> [in] [IMAPITable::GetStatus](imapitable-getstatus.md) の一部としてクライアント アプリケーションまたはサービス プロバイダーが使用できるテーブルの種類は、そのテーブル ビューのデータを返します。 使用可能な値は次のいずれかです。 
    
TBLTYPE_DYNAMIC 
  
> テーブルの内容は動的であり、基になるデータの変更に応じ変更できます。 
    
TBLTYPE_KEYSET 
  
> テーブル内の行は固定されますが、これらの行の値は動的であり、基になるデータが変更されるに従って変更される可能性があります。 
    
TBLTYPE_SNAPSHOT 
  
> テーブルは静的であり、基になるデータが変更された場合、内容は変更されません。 
    
 _ulPropTagIndexColumn_
  
> [in]テーブル データを変更するときに使用する列のインデックス番号。 
    
 _lpSPropTagArrayColumns_
  
> [in]オブジェクトがデータを保持するテーブルで必要なプロパティを示すプロパティ タグの配列を含む [SPropTagArray](sproptagarray.md) 構造体へのポインター。 
    
 _lppTableData_
  
> [out]返されるテーブル データ オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

_lpAllocateBuffer_ _、lpAllocateMore、lpFreeBuffer_ 入力パラメーターは [、MAPIAllocateBuffer、MAPIAllocateMore、MAPIFreeBuffer](mapiallocatebuffer.md)関数をそれぞれ指します。  [](mapiallocatemore.md) [](mapifreebuffer.md) CreateTable を呼び **出すクライアント アプリケーション** は、という名前の MAPI 関数へのポインターを渡します。サービス プロバイダーは、初期化呼び出しで受け取った、 [または IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) メソッドへの呼び出しで取得したこれらの関数へのポインターを渡します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable : IUnknown](imapitableiunknown.md)

