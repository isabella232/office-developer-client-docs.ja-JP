---
title: IFreeBusySupportLoadFreeBusyData
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f0baa310-7a53-07ee-0a7d-33dd1fb465c2
description: 指定したユーザーごとに、時間範囲内のデータの空き時間情報ブロックを列挙するインターフェイスを返します。
ms.openlocfilehash: e55f902117a20bfefaa5d9a2f3a067cb78ec86cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411233"
---
# <a name="ifreebusysupportloadfreebusydata"></a>IFreeBusySupport::LoadFreeBusyData

指定したユーザーごとに、時間範囲内のデータの空き時間情報ブロックを列挙するインターフェイスを返します。 
  
## <a name="quick-info"></a>クイック ヒント

[「IFreeBusySupport」を参照してください](ifreebusysupport.md)。
  
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

_cMax_
  
> [in]返す [IFreeBusyData](ifreebusydata.md) インターフェイスの数。 
    
_rgfbuser_
  
> [in]データを取得する空き時間情報ユーザーの配列。
    
_prgfbdata_
  
> [in][out][FBUser](fbuser.md)構造体の _rgfbuser_ 配列に対応する **IFreeBusyData** インターフェイスの配列。 
    
   > [!NOTE]
   > このポインターの配列は、呼び出し元によって割り当て、呼び出し元によって解放されます。 呼び出し元が呼び出し元と一緒に実行されると、指す実際のインターフェイスが解放されます。 
  
_phrStatus_
  
> [out] **HRESULT の配列は** 、対応する各 **IFreeBusyData インターフェイスを取得するための結果** です。 値には NULL を指定できます。 対応する  _prgfbdata_ が有効S_OK場合、結果は値に設定されます。 
    
_pcRead_
  
>  [out] **IFreeBusyData** インターフェイスが見つかったユーザーの実際の数。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="see-also"></a>関連項目

- [定数 (空き時間情報 API)](constants-free-busy-api.md)

