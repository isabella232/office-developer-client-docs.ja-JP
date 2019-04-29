---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: 指定した各ユーザーについて、時間範囲内のデータの空き時間ブロックを列挙するためのインターフェイスを返します。
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411233"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

指定した各ユーザーについて、時間範囲内のデータの空き時間ブロックを列挙するためのインターフェイスを返します。 
  
## <a name="quick-info"></a>クイック ヒント

[IFreeBusySupport](ifreebusysupport.md)を参照してください。
  
```cpp
HRESULT LoadFreeBusyData( 
    ULONG cMax,  
    FBUser *rgfbuser, 
    IFreeBusyData **prgfbdata,  
    HRESULT *phrStatus, 
    ULONG *pcRead 
);
```

## <a name="parameters"></a>パラメーター

_cmax_
  
> 順番取得する[IFreeBusyData](ifreebusydata.md)インターフェイスの数を指定します。 
    
_rgfbuser_
  
> 順番データを取得する空き時間情報ユーザーの配列。
    
_prgfbdata_
  
> 順番読み上げ[fbuser](fbuser.md)構造の_rgfbuser_配列に対応する**IFreeBusyData**インターフェイスの配列。 
    
   > [!NOTE]
   > このポインターの配列は、呼び出し元によって割り当てられ、呼び出し元によって解放されます。 呼び出し元が実行されたときに、参照されている実際のインターフェイスは解放されます。 
  
_phrStatus_
  
> 読み上げそれぞれの対応する**IFreeBusyData**インターフェイスを取得するための**HRESULT**結果の配列。 値は NULL である場合があります。 対応する_prgfbdata_が有効な場合、結果は S_OK に設定されます。 
    
_pcread_
  
>  読み上げ**IFreeBusyData**インターフェイスが検出された実際のユーザー数。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [定数 (空き時間情報 API)](constants-free-busy-api.md)

