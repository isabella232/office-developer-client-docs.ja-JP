---
title: IFreeBusyDataEnumBlocks
manager: soliver
ms.date: 02/18/2016
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0cd5a5ae-118f-c7da-4eda-e97590fc39d4
description: 指定した時間範囲内のユーザーのデータのブロックの空き時間情報を列挙するインターフェイスを取得します。
ms.openlocfilehash: 51a77b2f47166628db07259ef841e0d6173ee370
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394539"
---
# <a name="ifreebusydataenumblocks"></a>IFreeBusyData::EnumBlocks

指定した時間範囲内のユーザーのデータのブロックの空き時間情報を列挙するインターフェイスを取得します。
  
## <a name="quick-info"></a>クイック ヒント

[IFreeBusyData](ifreebusydata.md)を参照してください。
  
```cpp
HRESULT EnumBlocks( 
     IEnumFBBlock **ppenumfb,  
     FILETIME ftmStart, 
     FILETIME ftmEnd 
);

```

## <a name="parameters"></a>パラメーター

_ppenumfb_
  
> [out]ブロックの空き時間情報を列挙するインターフェイスです。
    
_ftmStart_
  
> [in]列挙体の開始時刻。 [FILETIME](https://msdn.microsoft.com/library/ 4af8e79a-697e-44a1-8576-fdc57726e9ef.aspx)で表されます。
    
_ftmEnd_
  
> [in]列挙の終了時間です。 **FILETIME**で表されます。 
    
## <a name="return-values"></a>戻り値

呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。
  
## <a name="remarks"></a>解釈

予定表のアイテムの詳細を取得するための時間の範囲を示すためにこのメソッドを使用します。 *FtmStart*と*ftmEnd*の値がキャッシュされ、 [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)の後続の呼び出しで返されます。
  
空き/予約済みのプロバイダーは返される[IEnumFBBlock](ienumfbblock.md)インターフェイスを使用してもその後、列挙体にアクセスします。 
  
## <a name="see-also"></a>関連項目

- [IEnumFBBlock](ienumfbblock.md)
- [IFreeBusyData::GetFBPublishRange](ifreebusydata-getfbpublishrange.md)
- [IFreeBusyData::SetFBRange](ifreebusydata-setfbrange.md)
- [空き時間情報データにアクセスするのに相対時間を使用する](how-to-use-relative-time-to-access-free-busy-data.md)

