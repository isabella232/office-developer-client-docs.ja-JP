---
title: ITableDataHrGetView
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrGetView
api_type:
- COM
ms.assetid: 0e2a47be-497b-4031-87ce-60b2635e25f7
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7567113d1247b55f1ee5a609964728980d928cac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613780"
---
# <a name="itabledatahrgetview"></a>ITableData::HrGetView

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
IMAPITable 実装へのポインターを返すテーブル [ビューを作成](imapitableiunknown.md) します。 
  
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
  
> [in]テーブル ビューの並べ替え順序を表す並べ替え順序構造へのポインター。 _lpSSortOrderSet_ パラメーターで NULL が渡された場合、ビューは並べ替えされません。 
    
 _lpfCallerRelease_
  
> [in]MAPI がビューを解放するときに呼び出す [CALLERRELEASE](callerrelease.md) プロトタイプに基づくコールバック関数へのポインター。 _lpfCallerRelease_ パラメーターで NULL が渡された場合、ビューのリリース時に関数は呼び出されません。 
    
 _ulCallerData_
  
> [in]新しいビューで保存し  _、lpfCallerRelease_ が指すコールバック関数に渡す必要があるデータ。
    
 _lppMAPITable_
  
> [out]新しく作成されたビューへのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> ビューが正常に作成されました。
    
## <a name="remarks"></a>注釈

**ITableData::HrGetView** メソッドは _、lpSSortOrderSet_ パラメーターが指す順序で並べ替え、テーブル内のデータの読み取り専用ビューを作成します。 カーソルは、ビューの最初の行の先頭に配置されます。 ビュー **にアクセスする IMAPITable** インターフェイス実装が返されます。 
  
サービス プロバイダーは、 **クライアントにテーブルへの** アクセス権を与える必要がある場合に HrGetView を呼び出します。 **HrGetView は** ビューを作成し **、IMAPITable ポインターを返** します。 サービス プロバイダーは、クライアントにポインターを渡します。 クライアントがテーブルの使用を終了し、 [その IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) メソッドを呼び出す場合 **、HrGetView** は  _lpfCallerRelease_ パラメーターが指すコールバック関数を呼び出します。 
  
サービス プロバイダーがカスタマイズされた列セットまたは制限を持つビューをクライアントに返す必要がある場合、プロバイダーは、クライアント アクセスを許可する前に、ビューの [IMAPITable::SetColumns](imapitable-setcolumns.md) メソッドと [IMAPITable::Restrict](imapitable-restrict.md) メソッドを呼び出すことができます。 
  
## <a name="see-also"></a>関連項目



[CALLERRELEASE](callerrelease.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[SSortOrderSet](ssortorderset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

