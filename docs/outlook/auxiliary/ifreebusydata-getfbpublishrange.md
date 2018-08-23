---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: ユーザーのデータのブロックの空き時間情報の列挙型の事前に設定された時間の範囲を取得します。
ms.openlocfilehash: 2a322a43da38a0b902789f4c83baaabd769154c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799337"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

ユーザーのデータのブロックの空き時間情報の列挙型の事前に設定された時間の範囲を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IFreeBusyData](ifreebusydata.md)を参照してください。
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>パラメーター

_prtmStart_
  
> [out]空き時間情報の開始時刻の相対的な値です。 この値は、1601 年 1 月 1 日以降の分の数です。
    
_prtmEnd_
  
> [out]空き時間情報の最後の時間の相対値です。 この値は、1601 年 1 月 1 日以降の分の数です。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

空き/予約済みのプロバイダーには、列挙体の時間範囲を設定するには、 [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)または[IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)が呼び出されます。 1601 年 4 月 1 日、00:00:00Z と 11:59:59Z が 4500 年 8 月 31 日間、 **prtmStart**および**prtmEnd**の既定値を設定する必要があります[IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)または[IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)のいずれかが呼び出されなかった場合、それぞれ。 さらに、開始時刻を終了時刻より大きい値を設定しないでください。 
  
**IFreeBusyData::GetFBPublishRange**は、 **IFreeBusyData::EnumBlocks**または**IFreeBusyData::SetFBRange**の最新の呼び出しによってキャッシュされた時間の範囲の値の設定を返す必要があります。 
  
## <a name="see-also"></a>関連項目

- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

