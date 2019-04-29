---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: ユーザーのデータの空き時間ブロックの列挙の事前設定の時間範囲を取得します。
ms.openlocfilehash: 26951ea6a885f8d0e5e6a2fb5bcf9a63069c7f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430078"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

ユーザーのデータの空き時間ブロックの列挙の事前設定の時間範囲を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IFreeBusyData](ifreebusydata.md)を参照してください。
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>パラメーター

_prtmstart_
  
> 読み上げ空き時間情報の開始の相対時間値。 この値は、1601年1月1日からの経過時間 (分単位) です。
    
_prtmEnd_
  
> 読み上げ空き時間情報の終了の相対時間値。 この値は、1601年1月1日からの経過時間 (分単位) です。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

空き時間情報プロバイダーは、 [IFreeBusyData:: enumblocks](ifreebusydata-enumblocks.md)または[IFreeBusyData:: setfbrange](ifreebusydata-setfbrange.md)を呼び出して、列挙の時間範囲を設定します。 [IFreeBusyData:: enumblocks](ifreebusydata-enumblocks.md)または[IFreeBusyData:: setfbrange](ifreebusydata-setfbrange.md)がまだ呼び出されていない場合は、 **prtmstart**および**prtmEnd**の既定値は4月1日、1601 00:00: 00z、4500 11 年8月31日の間に設定する必要があります。59z4.3. さらに、開始時刻を終了時刻よりも大きい値に設定することはできません。 
  
**IFreeBusyData:: getfbpublishrange**は、 **IFreeBusyData:: enumblocks**または**IFreeBusyData:: setfbrange**最新の呼び出しによって設定された時間範囲のキャッシュされた値を返す必要があります。 
  
## <a name="see-also"></a>関連項目

- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

