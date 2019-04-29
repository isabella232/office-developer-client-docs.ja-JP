---
title: imapisupportgetoneofftable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetOneOffTable
api_type:
- COM
ms.assetid: 6800fd3a-aa43-45fe-9cc2-102d0ef43edf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c0beec8a0b234794d3f623c4ceac773db698dd79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412759"
---
# <a name="imapisupportgetoneofftable"></a>IMAPISupport::GetOneOffTable

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI の1回限りのテーブルへのポインター (すべてのアドレス帳プロバイダーが新しい受信者を作成するためにサポートするテンプレートのリスト) を返します。
  
```cpp
HRESULT GetOneOffTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>パラメーター

 _ulFlags_
  
> 順番文字列列の種類を制御するフラグのビットマスク。 次のフラグを設定できます。
    
MAPI_UNICODE 
  
> 文字列列は Unicode 形式です。 MAPI_UNICODE フラグが設定されていない場合、文字列列は ANSI 形式になります。
    
 _lpptable_
  
> 読み上げ1回限りのテーブルへのポインターへのポインター。
    
## <a name="return-value"></a>戻り値

S_OK 
  
> 1回限りのテーブルが正常に取得されました。
    
## <a name="remarks"></a>注釈

**imapisupport:: getoneofftable**メソッドは、アドレス帳プロバイダーサポートオブジェクトに対して実装されています。 アドレス帳プロバイダーは、 **getoneofftable**を呼び出して、新しい受信者を作成するためのテンプレートの完全なリストを取得します。 この表には、セッションのサポートでアクティブになっているブックプロバイダーと MAPI がサポートするテンプレートのテンプレートが含まれています。 
  
新しく作成された受信者を使用して、メッセージの宛先を指定することも、アドレス帳コンテナーに追加することもできます。
  
1回限りのテーブルで必要な列セットを構成するプロパティの一覧については、「 [1 回限りのテーブル](one-off-tables.md)」を参照してください。
  
_ulflags_パラメーターの MAPI_UNICODE フラグを設定すると、 [imapitable:: querycolumns](imapitable-querycolumns.md)および[imapitable:: QueryRows](imapitable-queryrows.md)メソッドから返される列の形式に影響します。 このフラグは、 [IMAPITable:: querysortorder](imapitable-querysortorder.md)メソッドによって返される並べ替え順序で、プロパティの種類を制御することもできます。 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

この1回限りのテーブルへの変更の通知を受信するように登録されている場合は、他のプロバイダーの1回限りのテーブルへの変更について通知を受け取ることもあります。 これらの通知に基づいて、現在のセッション中に追加された新しいアドレスの種類をサポートできます。
  
## <a name="see-also"></a>関連項目



[IABContainer::CreateEntry](iabcontainer-createentry.md)
  
[IMAPISupport::NewEntry](imapisupport-newentry.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[IMAPITable::QueryColumns](imapitable-querycolumns.md)
  
[IMAPITable::QueryRows](imapitable-queryrows.md)
  
[IMAPITable::QuerySortOrder](imapitable-querysortorder.md)
  
[PidTagCreateTemplates 標準プロパティ](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)


[1回限りのテーブル](one-off-tables.md)

