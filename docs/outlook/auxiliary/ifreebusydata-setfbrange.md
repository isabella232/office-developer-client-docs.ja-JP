---
title: IFreeBusyDataSetFBRange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e7147ea-0eb0-324a-80d8-4f0eef654c32
description: ユーザーのデータの空き時間ブロックの列挙時間の範囲を設定します。
ms.openlocfilehash: 4647453acb0e530521aa808f7f017e3e311644bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421663"
---
# <a name="ifreebusydatasetfbrange"></a>IFreeBusyData::SetFBRange

ユーザーのデータの空き時間ブロックの列挙時間の範囲を設定します。
  
## <a name="quick-info"></a>クイック ヒント

[IFreeBusyData](ifreebusydata.md)を参照してください。
  
```cpp
HRESULT SetFBRange(
     LONG rtmStart,
     LONG rtmEnd
);
```

## <a name="parameters"></a>パラメーター

_rtmstart_
  
> 順番空き時間情報の開始の相対時間値。 この値は、1601年1月1日からの経過時間 (分単位) です。
    
_rtmEnd_
  
> 順番空き時間情報の終了の相対時間値。 この値は、1601年1月1日からの経過時間 (分単位) です。
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

このメソッドは、詳細を取得する予定表アイテムの時間範囲を示すために使用されます。 *ftmstart*および*ftmEnd*の値はキャッシュされ、その後の[IFreeBusyData:: getfbpublishrange](ifreebusydata-getfbpublishrange.md)の呼び出しで返されます。
  
## <a name="see-also"></a>関連項目

- [IFreeBusyData::EnumBlocks](ifreebusydata-enumblocks.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)

