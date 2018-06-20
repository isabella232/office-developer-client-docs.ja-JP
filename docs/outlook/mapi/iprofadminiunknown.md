---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c6192e6f92078f2f9bab0d55e9952d21ebb82af6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801136"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin: IUnknown

  
  
**適用されます**: Outlook 
  
プロファイルの管理をサポートしています。 
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapix.h  <br/> |
|によって公開されます。  <br/> |プロファイル管理オブジェクト  <br/> |
|によって実装されます。  <br/> |MAPI  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーション  <br/> |
|インターフェイスの識別子。  <br/> |IID_IProfAdmin  <br/> |
|ポインターの型。  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[発生しました](iprofadmin-getlasterror.md) <br/> |前のプロファイルの管理オブジェクトに発生したエラーに関する情報を格納する[MAPIERROR](mapierror.md)構造体を返します。  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |プロファイル テーブルのすべての利用可能なプロファイルに関する情報を格納するテーブルへのアクセスを提供します。  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |新しいプロファイルを作成します。  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |プロファイルを削除します。  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |現在は廃止されています。 プロファイルのパスワードを変更します。  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |プロファイルをコピーします。  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |プロファイルに新しい名前が割り当てられます。  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |設定またはクライアントの既定のプロファイルを削除します。  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |プロファイル内のメッセージ サービスを変更する場合、メッセージ サービスの管理オブジェクトへのアクセスを提供します。  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI インターフェイス](mapi-interfaces.md)

