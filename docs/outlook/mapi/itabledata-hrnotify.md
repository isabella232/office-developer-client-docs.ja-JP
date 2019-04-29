---
title: itabledatahrnotify
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
  
表の行の通知を送信します。
  
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
    
 _cvalues_
  
> 順番_lpspropvalue_パラメーターによってポイントされている[spropvalue](spropvalue.md)構造のプロパティ値の数。 
    
 _lpspropvalue_
  
> 順番ターゲット行の列の値を記述する**spropvalue**構造体へのポインター。 
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>注釈

**itabledata:: hrnotify**メソッドは、 _lpspropvalue_パラメーターで指定されたプロパティによって示される行に一致する行に対して TABLE_ROW_MODIFIED 通知を送信します。 **hrnotify**は、変更が行に対して発生したかどうかにかかわらず通知を送信します。 表のビューを持つすべてのクライアントおよびサービスプロバイダーは、 [「IMAPITable:: アドバイス](imapitable-advise.md)」を参照して、この通知を受信します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

