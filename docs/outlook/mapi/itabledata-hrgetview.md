---
title: itabledatahrgetview
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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 375a0f1d39b09b7ad453120f20752e00ffda0e15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278716"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPITable](imapitableiunknown.md)実装へのポインターを返すテーブルビューを作成します。 
  
```cpp
HRESULT HrGetView(
  LPSSortOrderSet lpSSortOrderSet,
  CALLERRELEASE FAR * lpfCallerRelease,
  ULONG_PTR ulCallerData,
  LPMAPITABLE FAR * lppMAPITable
);
```

## <a name="parameters"></a>パラメーター

 _lpssortorderset_
  
> 順番テーブルビューの並べ替え順序を記述する並べ替え順序構造体へのポインター。 _lpssortorderset_パラメーターで NULL が渡された場合、ビューは並べ替えられません。 
    
 _lpfcallerrelease_
  
> 順番ビューを解放したときに MAPI が呼び出す呼び出し[errelease](callerrelease.md)プロトタイプに基づく、コールバック関数へのポインター。 _lpfcallerrelease_パラメーターで NULL が渡された場合、ビューのリリース時に関数は呼び出されません。 
    
 _ulcallerdata_
  
> 順番新しいビューで保存する必要があり、 _lpfcallerrelease_が指すコールバック関数に渡されるデータ。
    
 _lppMAPITable_
  
> 読み上げ新しく作成されたビューへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ビューが正常に作成されました。
    
## <a name="remarks"></a>解説

**itabledata:: hrgetview**メソッドは、テーブル内のデータの読み取り専用のビューを作成します。これは、 _lpssortorderset_パラメーターで示された順序で並べ替えられます。 カーソルは、ビューの最初の行の先頭に配置されます。 ビューにアクセスするための**IMAPITable**インターフェイスの実装が返されます。 
  
サービスプロバイダーは、クライアントがテーブルにアクセスできるようにする必要がある場合に**hrgetview**を呼び出します。 **hrgetview**はビューを作成し、 **IMAPITable**ポインターを返します。 その後、サービスプロバイダーはクライアントにポインターを渡します。 表を使用してクライアントが終了し、その[IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx)メソッドを呼び出すと、 **hrgetview**は_lpfcallerrelease_パラメーターで指定されたコールバック関数を呼び出します。 
  
サービスプロバイダーが、カスタマイズされた列セットまたは制限を持つビューをクライアントに戻す必要がある場合、プロバイダーはクライアントアクセスを許可する前に、ビューの[IMAPITable:: SetColumns](imapitable-setcolumns.md)および[imapitable:: Restrict](imapitable-restrict.md)メソッドを呼び出すことができます。 
  
## <a name="see-also"></a>関連項目



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

