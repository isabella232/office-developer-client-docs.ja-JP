---
title: imapiprop IUnknown
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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407663"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアント、サービスプロバイダ、MAPI がプロパティを使用できるようにします。 プロパティをサポートするすべてのオブジェクトは、このインターフェイスを実装します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |このインターフェイスを直接公開するオブジェクトはありません。  <br/> |
|実装元:  <br/> |サービスプロバイダーと MAPI  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーション、サービスプロバイダー、MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIProp  <br/> |
|ポインターの種類:  <br/> |LPMAPIPROP  <br/> |
|トランザクションモデル:  <br/> |抽象クラス、実装されていません  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |前のエラーについての情報を含む[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |前回の保存操作以降にオブジェクトに加えられたすべての変更を永続的に行います。  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |オブジェクトの1つ以上のプロパティのプロパティ値を取得します。  <br/> |
|[getproplist](imapiprop-getproplist.md) <br/> |すべてのプロパティのプロパティタグを返します。  <br/> |
|[openproperty](imapiprop-openproperty.md) <br/> |プロパティへのアクセスに使用できるインターフェイスへのポインターを返します。  <br/> |
|[setprops による](imapiprop-setprops.md) <br/> |1つまたは複数のプロパティを更新します。  <br/> |
|[deleteprops](imapiprop-deleteprops.md) <br/> |オブジェクトから1つ以上のプロパティを削除します。  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |明示的に除外されているプロパティ以外のすべてのプロパティをコピーまたは移動します。  <br/> |
|[copyprops](imapiprop-copyprops.md) <br/> |選択されたプロパティをコピーまたは移動します。  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |1つまたは複数のプロパティ識別子に対応するプロパティ名を提供します。  <br/> |
|[getidsfromnames](imapiprop-getidsfromnames.md) <br/> |1つまたは複数のプロパティ名に対応するプロパティ識別子を提供します。  <br/> |
   
## <a name="remarks"></a>注釈

 **imapiprop**は、次のインターフェイスの基本インターフェイスです。 
  
- [iattach](iattachimapiprop.md)
    
- [imailuser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [imapiforminfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [ipropdata](ipropdataimapiprop.md)
    
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

