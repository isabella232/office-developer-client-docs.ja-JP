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
  
**IStream**オブジェクトに**IStorage**インターフェイスを階層的に配置します。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiutil  <br/> |
|実装元:  <br/> |MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーションとサービスプロバイダー  <br/> |
   
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
  
> 順番**IStream**を実装している**IUnknown**オブジェクトへのポインター。 
    
 _lpinterface_
  
> 順番stream オブジェクトのインターフェイス識別子 (IID) へのポインター。 _lpinterface_パラメーターには、次のいずれかの値を渡すことができます。 NULL、IID_IStream、または IID_ILockBytes。 _lpinterface_で NULL を渡すことは、IID_IStream を渡すことと同じです。 
    
 _ulFlags_
  
> 順番ストリームに対するストレージオブジェクトの作成方法を制御するフラグのビットマスク。 既定の設定は STGSTRM_RESET です。これにより、ストレージオブジェクトの読み取り専用アクセスが可能になり、ストリームの0の位置で開始されます。 次のフラグを任意の組み合わせで設定できます (記載されている場合を除く)。
    
STGSTRM_CREATE 
  
> stream オブジェクトの新しいストレージオブジェクトを作成します。 STGSTRM_RESET フラグが設定されている場合、このフラグは設定できません。 
    
STGSTRM_CURRENT 
  
> ストリームの現在の位置でストレージを開始します。 STGSTRM_RESET フラグが設定されている場合、このフラグは設定できません。 
    
STGSTRM_MODIFY 
  
> 呼び出し元のサービスプロバイダーが、返されたストレージに書き込むことができるようにします。 STGSTRM_RESET フラグが設定されている場合、このフラグは設定できません。 
    
STGSTRM_RESET 
  
> 位置0でストレージを開始します。 他のフラグが設定されている場合、このフラグを設定することはできません。 
    
 _lppstorageout_
  
> 読み上げ返された**IStorage**オブジェクトへのポインターへのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

メッセージストアプロバイダーは、添付ファイル用の**IStorage**インターフェイスを使用して、 **hristoragefromstream**関数をサポートします。 ストアプロバイダーは、 **IStream**インターフェイスを実装する必要があります。 **hristoragefromstream**は、 **IStream**オブジェクトの**IStorage**インターフェイスを提供します。 _lpUnkIn_では、 **ILockBytes**または**IStream**インターフェイスのいずれかを渡すことができます。 
  

