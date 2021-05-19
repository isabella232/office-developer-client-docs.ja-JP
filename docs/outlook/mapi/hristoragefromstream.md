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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416833"
---
# <a name="hristoragefromstream"></a>HrIStorageFromStream

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**IStorage インターフェイスを** **IStream オブジェクトにレイヤー** します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil.h  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーションとサービス プロバイダー  <br/> |
   
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
  
> [in] **IStream を実装する IUnknown** オブジェクト **へのポインター**。 
    
 _lpInterface_
  
> [in]ストリーム オブジェクトのインターフェイス識別子 (IID) へのポインター。 _lpInterface_ パラメーターには、NULL、IID_IStream、またはIID_ILockBytes。 _lpInterface で NULL を渡す_ のは、引数を渡すのとIID_IStream。 
    
 _ulFlags_
  
> [in]ストリームを基準にストレージ オブジェクトを作成する方法を制御するフラグのビットマスク。 既定の設定は、STGSTRM_RESETオブジェクトに読み取り専用アクセス権を与え、ストリームの位置 0 から開始します。 以下のフラグは、以下に示す以外の任意の組み合わせで設定できます。
    
STGSTRM_CREATE 
  
> ストリーム オブジェクトの新しいストレージ オブジェクトを作成します。 このフラグは、このフラグがSTGSTRM_RESET設定されている場合は設定できません。 
    
STGSTRM_CURRENT 
  
> ストリームの現在の位置で記憶域を開始します。 このフラグは、このフラグがSTGSTRM_RESET設定されている場合は設定できません。 
    
STGSTRM_MODIFY 
  
> 呼び出し元のサービス プロバイダーが返された記憶域に書き込みを許可します。 このフラグは、このフラグがSTGSTRM_RESET設定されている場合は設定できません。 
    
STGSTRM_RESET 
  
> 位置 0 で記憶域を開始します。 他のフラグが設定されている場合は、このフラグを設定できません。 
    
 _lppStorageOut_
  
> [out]返される **IStorage オブジェクトへのポインターへの** ポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

メッセージ ストア プロバイダーは、添付ファイルの IStorage インターフェイスを使用して **HrIStorageFromStream** **関数** をサポートします。 ストア プロバイダーは **、IStream インターフェイスを実装する必要** があります。 **HrIStorageFromStream** は **、IStream オブジェクトの IStorage** インターフェイス **を提供** します。 lpUnkIn で **ILockBytes** または **IStream** インターフェイスを渡  _す可能性があります_。 
  

