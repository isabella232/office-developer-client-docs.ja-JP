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
ms.openlocfilehash: 651ef6a7c1af70c75a85e13414c4fd7632d30290
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800546"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**適用対象**: Outlook 
  
分散コンピューティング環境では、構成可能な実行時のフォームの使用をサポートしています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|によって公開されます。  <br/> |ファクトリ オブジェクトのフォーム  <br/> |
|によって実装されます。  <br/> |フォーム サーバー  <br/> |
|によって呼び出されます。  <br/> |フォームの閲覧者  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMAPIFormFactory  <br/> |
|ポインターの型。  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |フォームのクラス ファクトリ オブジェクトを返します。  <br/> |
|[発生しました](imapiformfactory-getlasterror.md) <br/> |前の工場出荷時のフォーム オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |開いているフォームのサーバーは、メモリ内に保持します。  <br/> |
   
## <a name="remarks"></a>注釈

[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx)インターフェイスは、 **IMAPIFormFactory**インターフェイスがベースし、 **IMAPIFormFactory**を実装するオブジェクトは、 **IClassFactory**からも継承する必要があります。
  
 **IMAPIFormFactory**は、フォーム サーバーが 1 つ以上のメッセージ クラスをサポートしている場合、新しいフォーム オブジェクトを作成するフォームの閲覧者が使用するインターフェイス (つまり、1 つ以上の入力フォームのオブジェクトの)。 
  
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

