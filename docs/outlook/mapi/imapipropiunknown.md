---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 02d2b136ed1437ba53ce1e54a202d70a48b2abe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800673"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**適用対象**: Outlook 
  
プロパティを操作するには、クライアント、サービス プロバイダー、および MAPI を有効にします。 プロパティをサポートするすべてのオブジェクトは、このインターフェイスを実装します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |オブジェクトは直接このインターフェイスを公開しません。  <br/> |
|によって実装されます。  <br/> |サービス プロバイダーおよび MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション、サービス プロバイダー、および MAPI  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIProp  <br/> |
|ポインターの型。  <br/> |LPMAPIPROP  <br/> |
|トランザクション モデル:  <br/> |抽象クラスで実装されることはありません。  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](imapiprop-getlasterror.md) <br/> |前のエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |前回の保存操作以降は、オブジェクトに対して行われた変更を永続的になります。  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |オブジェクトの 1 つまたは複数のプロパティのプロパティ値を取得します。  <br/> |
|[Getproplist メソッド](imapiprop-getproplist.md) <br/> |すべてのプロパティのプロパティ タグを返します。  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |プロパティにアクセスするために使用するインターフェイスへのポインターを返します。  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |1 つまたは複数のプロパティを更新します。  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |オブジェクトから 1 つまたは複数のプロパティを削除します。  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |明確に除外されたプロパティ以外のすべてのプロパティを移動またはコピーします。  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |選択したプロパティのコピーまたは移動します。  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |1 つまたは複数のプロパティの識別子に対応するプロパティ名を提供します。  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |1 つまたは複数のプロパティ名に対応するプロパティの識別子を提供します。  <br/> |
   
## <a name="remarks"></a>注釈

 **IMAPIProp**は、次のインターフェイスの基本インターフェイスです。 
  
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



[MAPI インターフェイス](mapi-interfaces.md)

