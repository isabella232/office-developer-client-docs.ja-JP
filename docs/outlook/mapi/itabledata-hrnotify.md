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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 20831901567f177ada70a6cea94db0537786db94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571438"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
テーブルの行の通知を送信します。
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulFlags_
  
> [����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B
    
 _あう_
  
> [in]_LpSPropValue_パラメーターが指す[SPropValue](spropvalue.md)構造体のプロパティ値の数です。 
    
 _lpSPropValue_
  
> [in]対象行の列の値を記述する**SPropValue**構造体へのポインター。 
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B
    
## <a name="remarks"></a>����

**ITableData::HrNotify**メソッドは、 _lpSPropValue_パラメーターで指定されたプロパティで示される行に一致する行の TABLE_ROW_MODIFIED の通知を送信します。 **HrNotify**は、行に変更があったかどうかに関係なく通知を送信します。 すべてのクライアントやテーブルのビューがあり、そのビューに通知を登録するのには[IMAPITable::Advise](imapitable-advise.md)としているサービス プロバイダーは、この通知を受信します。 
  
## <a name="see-also"></a>関連項目



[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

