---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: ユーザーのデータの空き時間情報ブロックの列挙の時間範囲を設定します。
ms.openlocfilehash: 9e4c61eedf511dd9852cfe8e0c36cff525964815
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572215"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

ユーザーのデータの空き時間情報ブロックの列挙の時間範囲を設定します。
  
## <a name="quick-info"></a>クイック ヒント

[「IFreeBusyData」を参照してください](ifreebusydata.md)。
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>パラメーター

_rtmStart_
  
> [in]空き時間情報の開始の相対時間値。 この値は、1601 年 1 月 1 日以降の分数です。
    
_rtmEnd_
  
> [in]空き時間情報の末尾の相対時間値。 この値は、1601 年 1 月 1 日以降の分数です。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

このメソッドは、詳細を取得する予定表アイテムの時間範囲を示すために使用されます。 *ftmStart と* *ftmEnd* の値はキャッシュされ [、IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)の後続の呼び出しで返されます。
  
## <a name="see-also"></a>関連項目

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)

