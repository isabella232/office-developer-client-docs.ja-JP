---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: a913f2f3a72a365ec7d5078eccf31c4212ca83a5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801222"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**適用対象**: Outlook 
  
[IMAPITable](imapitableiunknown.md)実装へのポインターを返す表形式ビューを作成します。 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>パラメーター

 _lpSSortOrderSet_
  
> [in]テーブル ビューの並べ替え順序を記述する並べ替え順序の構造体へのポインター。 _LpSSortOrderSet_パラメーターに NULL を渡した場合、ビューは並べ替えられません。 
    
 _lpfCallerRelease_
  
> [in]MAPI がビューを解放するときに呼び出す[CALLERRELEASE](callerrelease.md)プロトタイプに基づいてコールバック関数へのポインター。 _LpfCallerRelease_パラメーターに NULL を渡した場合、ビューのリリースで関数は呼び出されません。 
    
 _ulCallerData_
  
> [in]_LpfCallerRelease_が指すデータを新しいビューを保存し、コールバック関数に渡される必要があります。
    
 _lppMAPITable_
  
> [out]新しく作成されたビューへのポインターへのポインター。
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> ビューは正しく作成されました。
    
## <a name="remarks"></a>注釈

**ITableData::HrGetView**メソッドは、 _lpSSortOrderSet_パラメーターで指定された順序で並べ替え、テーブルのデータの読み取り専用ビューを作成します。 カーソルは、ビューの最初の行の先頭に配置されます。 ビューにアクセスするため**IMAPITable**インターフェイスの実装が返されます。 
  
サービス プロバイダーは、テーブルにクライアントのアクセスを提供する必要があるときに**HrGetView**を呼び出します。 **HrGetView**では、ビューを作成し、 **IMAPITable**ポインターを返します。 サービス プロバイダーは、クライアントへのポインターを渡します。 クライアントでは、テーブルを使用した後し、その[リ ス](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)のメソッドを呼び出して、 **HrGetView**は、 _lpfCallerRelease_パラメーターで指定されたコールバック関数を呼び出します。 
  
サービス プロバイダーは、設定、カスタマイズされた列を持つビューをクライアントに返す必要があるか、制限、プロバイダー メソッドを呼び出して、ビューの[IMAPITable::SetColumns](imapitable-setcolumns.md)と[IMAPITable::Restrict](imapitable-restrict.md)のクライアント アクセスを許可する前にします。 
  
## <a name="see-also"></a>関連項目



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

