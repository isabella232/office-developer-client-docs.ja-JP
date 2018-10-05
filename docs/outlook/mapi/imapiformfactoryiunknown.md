---
title: IMAPIFormFactory IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormFactory
api_type:
- COM
ms.assetid: 637be364-c393-430a-84b3-2c96aa553c22
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384767"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
分散コンピューティング環境では、構成可能な実行時のフォームの使用をサポートしています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |ファクトリ オブジェクトのフォーム  <br/> |
|実装元:  <br/> |フォーム サーバー  <br/> |
|呼び出し元:  <br/> |フォームの閲覧者  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIFormFactory  <br/> |
|ポインターの型。  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |フォームのクラス ファクトリ オブジェクトを返します。  <br/> |
|[発生しました](imapiformfactory-getlasterror.md) <br/> |前の工場出荷時のフォーム オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |開いているフォームのサーバーは、メモリ内に保持します。  <br/> |
   
## <a name="remarks"></a>備考

[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx)インターフェイスは、 **IMAPIFormFactory**インターフェイスがベースし、 **IMAPIFormFactory**を実装するオブジェクトは、 **IClassFactory**からも継承する必要があります。
  
 **IMAPIFormFactory**は、フォーム サーバーが 1 つ以上のメッセージ クラスをサポートしている場合、新しいフォーム オブジェクトを作成するフォームの閲覧者が使用するインターフェイス (つまり、1 つ以上の入力フォームのオブジェクトの)。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

