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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5f42e1eb0d120d2fbb785e63b451acdd2d5a91f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799874"
---
# <a name="createtable"></a>CreateTable

  
  
**適用されます**: Outlook 
  
構造とテーブルの内容を作成するのに使用できる[ITableData](itabledataiunknown.md)オブジェクトのオブジェクト ハンドルを作成します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
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

## <a name="parameters"></a>Parameters

 _lpInterface_
  
> [in]テーブルのデータ オブジェクトのインターフェイス id (IID) へのポインター。 有効なインタ フェース識別子は、IID_IMAPITableData です。 テーブルのデータ オブジェクトの標準的なインターフェイスにキャストするのには_lppTableData_パラメーターで返されるテーブルのデータ オブジェクトは、 _lpInterface_パラメーターに NULL を渡すことも。 
    
 _lpAllocateBuffer_
  
> [in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。 
    
 _lpAllocateMore_
  
> [in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。 
    
 _lpFreeBuffer_
  
> [in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。 
    
 _lpvReserved_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B 
    
 _ulTableType_
  
> [in]表形式ビューの[IMAPITable::GetStatus](imapitable-getstatus.md)の戻り値のデータの一部としてクライアント アプリケーションまたはサービス プロバイダーに提供されるテーブルの型。 使用可能な値は次のとおりです。 
    
TBLTYPE_DYNAMIC 
  
> テーブルの内容は動的で、基になるデータの変化に応じて変更できます。 
    
TBLTYPE_KEYSET 
  
> テーブル内の行は固定ですが、これらの行の値は動的で、基になるデータの変化に応じて変更できます。 
    
TBLTYPE_SNAPSHOT 
  
> テーブルは静的であり、基になるデータが変更された内容も変更されません。 
    
 _ulPropTagIndexColumn_
  
> [in]テーブルのデータを変更するときに使用される列のインデックス番号です。 
    
 _lpSPropTagArrayColumns_
  
> [in]オブジェクト データを保持するテーブルに必要なプロパティを示すプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。 
    
 _lppTableData_
  
> [out]返されるテーブルのデータ オブジェクトへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

_LpAllocateBuffer_、 _lpAllocateMore_、および_lpFreeBuffer_の入力パラメーターは、それぞれ[MAPIAllocateBuffer](mapiallocatebuffer.md)、 [MAPIAllocateMore](mapiallocatemore.md)、および[MAPIFreeBuffer](mapifreebuffer.md)関数では、] をポイントします。 **CreateTable**を呼び出すクライアント アプリケーションが MAPI の関数を同じ名前でポインターを渡しますサービス プロバイダーの初期化の呼び出しで受信した、 [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)メソッドの呼び出しで取得するこれらの関数へのポインターを渡します。 
  
## <a name="see-also"></a>関連項目



[IMAPITable: IUnknown](imapitableiunknown.md)

