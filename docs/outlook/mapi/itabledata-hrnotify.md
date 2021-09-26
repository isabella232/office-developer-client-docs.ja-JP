---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: b89aef1aff41f7fd1f84d687c72d37ce306cc31e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610399"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
テーブル行の通知を送信します。
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _cValues_
  
> [in]_lpSPropValue_ パラメーターが指す [SPropValue](spropvalue.md)構造体のプロパティ値の数。 
    
 _lpSPropValue_
  
> [in]ターゲット行の列の値を記述する **SPropValue** 構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

**ITableData::HrNotify** メソッドは _、lpSPropValue_ パラメーターが示すプロパティで説明されている行に一致する行に対して TABLE_ROW_MODIFIED 通知を送信します。 **HrNotify は** 、行に変更が発生したかどうかに関係なく通知を送信します。 テーブルのビューを持ち [、IMAPITable::Advise](imapitable-advise.md) を呼び出しているすべてのクライアントとサービス プロバイダーは、ビューに関する通知を登録するためにこの通知を受け取ります。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

