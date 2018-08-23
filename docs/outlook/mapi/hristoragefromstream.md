---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 39f28d5a8e9c8c7f3dfc6a8d09cf022cea08800c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563925"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
**IStream**オブジェクト上に**IStorage**インターフェイスをレイヤーにします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションとサービス ・ プロバイダー  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>パラメーター

 _lpUnkIn_
  
> [in]**IStream**を実装する**IUnknown**オブジェクトへのポインター。 
    
 _lpInterface_
  
> [in]ストリーム オブジェクトのインターフェイス id (IID) へのポインター。 _LpInterface_パラメーターの値は次のいずれかに渡すことができます: NULL、IID_IStream、または IID_ILockBytes。 _LpInterface_に NULL を渡すことは、IID_IStream を渡すのと同じです。 
    
 _ulFlags_
  
> [in]記憶域オブジェクトのストリームを基準に作成する方法を制御するフラグのビットマスクです。 既定の設定は、ストレージ ・ オブジェクトの読み取り専用アクセスを提供し、ストリームの位置は 0 から始まり、STGSTRM_RESET です。 次のフラグは、前述のように、以外の組み合わせで設定できます。
    
STGSTRM_CREATE 
  
> ストリーム オブジェクトの新しいストレージ オブジェクトを作成します。 STGSTRM_RESET フラグが設定されている場合は、このフラグを設定することはできません。 
    
STGSTRM_CURRENT 
  
> ストレージ、ストリームの現在位置を開始します。 STGSTRM_RESET フラグが設定されている場合は、このフラグを設定することはできません。 
    
STGSTRM_MODIFY 
  
> 返された記憶域への書き込みに呼び出し元のサービス プロバイダーを使用できます。 STGSTRM_RESET フラグが設定されている場合は、このフラグを設定することはできません。 
    
STGSTRM_RESET 
  
> 0 の位置に記憶域を開始します。 他のフラグが設定されている場合は、このフラグを設定することはできません。 
    
 _lppStorageOut_
  
> [out]返された**IStorage**オブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

メッセージは、プロバイダーのサポート**IStorage**インターフェイスを使用して添付ファイルの**HrIStorageFromStream**関数を格納します。 ストア プロバイダーは、 **IStream**インターフェイスを実装する必要があります。 **HrIStorageFromStream**は、 **IStream**オブジェクトの**IStorage**インターフェイスを提供します。 **ILockBytes**または_lpUnkIn_の**IStream**インターフェイスのいずれかを渡すことは。 
  

