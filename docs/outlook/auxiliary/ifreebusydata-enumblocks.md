---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: 指定した時間範囲内のユーザーのデータの空き時間情報ブロックを列挙するインターフェイスを取得します。
ms.openlocfilehash: d33d4718707b44c481e5e54be47e4dad6b3b6bfa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572222"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

指定した時間範囲内のユーザーのデータの空き時間情報ブロックを列挙するインターフェイスを取得します。
  
## <a name="quick-info"></a>クイック ヒント

[「IFreeBusyData」を参照してください](ifreebusydata.md)。
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>パラメーター

_ppenumfb_
  
> [out]空き時間情報ブロックを列挙するインターフェイス。
    
_ftmStart_
  
> [in]列挙の開始時刻。 これは [FILETIME で表されます](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)。
    
_ftmEnd_
  
> [in]列挙の終了時刻。 これは **FILETIME で表されます**。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>注釈

このメソッドは、詳細を取得する予定表アイテムの時間範囲を示すために使用されます。 *ftmStart と* *ftmEnd* の値はキャッシュされ [、IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)の後続の呼び出しで返されます。
  
空き時間情報プロバイダーは、その後、返された [IEnumFBBlock](ienumfbblock.md) インターフェイスを使用して列挙にアクセスすることもできます。 
  
## <a name="see-also"></a>関連項目

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)

