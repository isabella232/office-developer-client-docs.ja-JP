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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c60b542852653bd617b5b9f604bbc44d575e5cb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342120"
---
# <a name="imapiformfactory--iunknown"></a>IMAPIFormFactory : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
分散コンピューティング環境での構成可能な実行時フォームの使用をサポートします。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform.h  <br/> |
|次のユーザーによって公開されます。  <br/> |フォーム ファクトリ オブジェクト  <br/> |
|実装元:  <br/> |フォーム サーバー  <br/> |
|呼び出し元:  <br/> |フォーム ビューアー  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFormFactory  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORMFACTORY  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[CreateClassFactory](imapiformfactory-createclassfactory.md) <br/> |フォームのクラス ファクトリ オブジェクトを返します。  <br/> |
|[GetLastError](imapiformfactory-getlasterror.md) <br/> |フォーム ファクトリ オブジェクトに発生した以前のエラーに関する情報を含む [MAPIERROR](mapierror.md) 構造体を返します。  <br/> |
|[LockServer](imapiformfactory-lockserver.md) <br/> |開いているフォーム サーバーをメモリに保持します。  <br/> |
   
## <a name="remarks"></a>注釈

**IMAPIFormFactory** インターフェイスは [IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx)インターフェイスに基づいており **、IMAPIFormFactory** を実装するオブジェクトも **IClassFactory から継承する必要があります**。
  
 **IMAPIFormFactory** は、フォーム サーバーが複数のメッセージ クラス (つまり、複数の種類のフォーム オブジェクト) をサポートする場合に、フォーム ビューアーが新しいフォーム オブジェクトを作成するために使用するインターフェイスです。 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

