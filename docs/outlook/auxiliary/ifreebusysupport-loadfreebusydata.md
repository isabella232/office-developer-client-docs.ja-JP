---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: ユーザーごとに指定された、時間の範囲内のデータのブロックの空き時間情報を列挙するためのインターフェイスを返します。
ms.openlocfilehash: 9af5a40da9f0a831de7346b44cee9ca004c02300
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799340"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

ユーザーごとに指定された、時間の範囲内のデータのブロックの空き時間情報を列挙するためのインターフェイスを返します。 
  
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

## <a name="parameters"></a>Parameters

_cMax_
  
> [in]返す[IFreeBusyData](ifreebusydata.md)のインタ フェースの数です。 
    
_rgfbuser_
  
> [in]データを取得するユーザーの空き時間情報の配列。
    
_prgfbdata_
  
> [in][out]_Rgfbuser_ [FBUser](fbuser.md)構造体の配列に対応する**IFreeBusyData**インターフェイスの配列。 
    
   > [!NOTE]
   > このポインターの配列は、呼び出し元によって割り当てられているし、呼び出し元によって解放されます。 示される実際のインターフェイスは、後に、呼び出し元に解放されます。 
  
_phrStatus_
  
> [out]**HRESULT**の配列は、それぞれ対応する**IFreeBusyData**インターフェイスを取得するため発生します。 値は NULL である可能性があります。 結果は、対応する_prgfbdata_が有効な場合は S_OK に設定されています。 
    
_pcRead_
  
>  [out]**IFreeBusyData**インタ フェースが検出されましたユーザーの実際の数です。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [定数 (空き時間情報の API)](constants-free-busy-api.md)

