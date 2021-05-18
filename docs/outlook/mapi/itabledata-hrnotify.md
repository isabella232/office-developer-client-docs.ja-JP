---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413270"
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

