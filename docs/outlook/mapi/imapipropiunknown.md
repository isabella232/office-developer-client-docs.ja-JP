---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 9f7667f4e1776b8aa5d6a455c847012328a35506
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567579"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント、サービス プロバイダー、MAPI がプロパティを操作できます。 プロパティをサポートするオブジェクトはすべて、このインターフェイスを実装します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |このインターフェイスを直接公開するオブジェクトはありません。  <br/> |
|実装元:  <br/> |サービス プロバイダーと MAPI  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション、サービス プロバイダー、MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIProp  <br/> |
|ポインターの種類:  <br/> |LPMAPIPROP  <br/> |
|トランザクション モデル:  <br/> |抽象クラス(実装されていない)  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |前のエラー [に関する](mapierror.md) 情報を含む MAPIERROR 構造体を返します。  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |最後の保存操作以降にオブジェクトに加えた変更を永続的に行います。  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |オブジェクトの 1 つ以上のプロパティのプロパティ値を取得します。  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |すべてのプロパティのプロパティ タグを返します。  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |プロパティへのアクセスに使用できるインターフェイスへのポインターを返します。  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |1 つ以上のプロパティを更新します。  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |オブジェクトから 1 つ以上のプロパティを削除します。  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |特定の除外プロパティを除くすべてのプロパティをコピーまたは移動します。  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |選択したプロパティをコピーまたは移動します。  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |1 つ以上のプロパティ識別子に対応するプロパティ名を指定します。  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |1 つ以上のプロパティ名に対応するプロパティ識別子を提供します。  <br/> |
   
## <a name="remarks"></a>注釈

 **IMAPIProp** は、次のインターフェイスの基本インターフェイスです。 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

