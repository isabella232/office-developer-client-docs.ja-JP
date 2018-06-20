---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: ユーザーの空き時間情報データ ブロックの列挙体の時間の範囲を設定します。
ms.openlocfilehash: 84a25a2dd43f594caa075d90e4f183086452184a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799355"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

ユーザーの空き時間情報データ ブロックの列挙体の時間の範囲を設定します。
  
## <a name="quick-info"></a>クイック ヒント

[IFreeBusyData](ifreebusydata.md)を参照してください。
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>Parameters

_rtmStart_
  
> [in]空き時間情報の開始時刻の相対的な値です。 この値は、1601 年 1 月 1 日以降の分の数です。
    
_rtmEnd_
  
> [in]空き時間情報の最後の時間の相対値です。 この値は、1601 年 1 月 1 日以降の分の数です。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

予定表のアイテムの詳細を取得するための時間の範囲を示すためにこのメソッドを使用します。 *FtmStart*と*ftmEnd*の値がキャッシュされ、 [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)の後続の呼び出しで返されます。
  
## <a name="see-also"></a>関連項目

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [空き時間情報データにアクセスする相対時間を使用します。](how-to-use-relative-time-to-access-free-busy-data.md)

