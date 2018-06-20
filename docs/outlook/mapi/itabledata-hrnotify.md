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
ms.openlocfilehash: 1be4fd95d29859c542fe553bdc3728ea23444694
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801234"
---
# <a name="itabledatahrnotify"></a>ITableData::HrNotify

  
  
**適用されます**: Outlook 
  
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
  
[ITableData: IUnknown](itabledataiunknown.md)

