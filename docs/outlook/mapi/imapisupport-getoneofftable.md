---
title: IMAPISupportGetOneOffTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 55958af9d68ac27a92f06528dbc8fbc1fc62e574
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556512"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI 一時テーブルへのポインター (すべてのアドレス帳プロバイダーが新しい受信者の作成をサポートするテンプレートの一覧) を返します。
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> [in]文字列列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 このフラグMAPI_UNICODE設定されていない場合、文字列列は ANSI 形式になります。
    
 _lppTable_
  
> [out]1 回表へのポインターを指すポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 1 回のテーブルが正常に取得されました。
    
## <a name="remarks"></a>注釈

**IMAPISupport::GetOneOffTable** メソッドは、アドレス帳プロバイダーサポート オブジェクトに実装されます。 アドレス帳プロバイダーは **GetOneOffTable** を呼び出して、新しい受信者を作成するためのテンプレートの完全な一覧を取得します。 この表には、セッション サポートでアクティブなアドレス帳プロバイダーのテンプレートと、MAPI がサポートするテンプレートが含まれています。 
  
新しく作成された受信者は、メッセージのアドレス指定に使用するか、アドレス帳コンテナーに追加できます。
  
1 回のテーブルで必要な列セットを作成するプロパティの一覧については [、「One-Off Tables」を参照してください](one-off-tables.md)。
  
_ulFlags_ パラメーター MAPI_UNICODEフラグを設定すると [、IMAPITable::QueryColumns](imapitable-querycolumns.md)および [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは [、IMAPITable::QuerySortOrder](imapitable-querysortorder.md) メソッドによって返される並べ替え順序のプロパティの種類も制御します。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

この一時テーブルに対する変更の通知を受け取る登録されている場合は、他のプロバイダーの一時テーブルに対する変更の通知も受け取る。 これらの通知に基づいて、現在のセッション中に追加される新しいアドレスの種類をサポートできます。
  
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[1 回切りテーブル](one-off-tables.md)

