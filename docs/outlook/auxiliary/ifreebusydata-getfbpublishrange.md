---
title: IFreeBusyDataGetFBPublishRange
manager: soliver
ms.date: 09/23/2016
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1a8bbe0c-17d1-9349-4c63-f257faf4edda
description: ユーザーのデータの空き時間情報ブロックの列挙の事前設定された時間範囲を取得します。
ms.openlocfilehash: 2480d781d5889515cbfe91c53a08a43436ed1d48
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614457"
---
# <a name="ifreebusydatagetfbpublishrange"></a>IFreeBusyData::GetFBPublishRange

ユーザーのデータの空き時間情報ブロックの列挙の事前設定された時間範囲を取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IFreeBusyData」を参照してください](ifreebusydata.md)。
  
```cpp
HRESULT GetFBPublishRange( 
     LONG *prtmStart,  
     LONG *prtmEnd 
);

```

## <a name="parameters"></a>パラメーター

_prtmStart_
  
> [out]空き時間情報の開始の相対時間値。 この値は、1601 年 1 月 1 日以降の分数です。
    
_prtmEnd_
  
> [out]空き時間情報の末尾の相対時間値。 この値は、1601 年 1 月 1 日以降の分数です。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

空き時間情報プロバイダーは [、IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md) または [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md) を呼び出して、列挙の時間範囲を設定します。 [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)または [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)が呼び出されていない場合 **、prtmStart** および **prtmEnd** の既定値は、それぞれ 1601 年 4 月 1 日 00:00:00Z から 8 月 31 日 11:59:59Z の間に設定する必要があります。 また、開始時刻を終了時刻より大きく設定する必要があります。 
  
**IFreeBusyData::GetFBPublishRange** は **、IFreeBusyData::EnumBlocks** または **IFreeBusyData::SetFBRange** の最新の呼び出しによって設定された時間範囲のキャッシュ値を返す必要があります。 
  
## <a name="see-also"></a>関連項目

- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)
- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)

