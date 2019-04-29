---
title: imapiforminfo imapiprop
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3913cb04f1f2f61ba6835b704f430d872756b227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417365"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントアプリケーションに、フォーム定義に特したプロパティへのアクセス権を付与します。 フォームの情報を別のオブジェクトに保持することにより、フォームライブラリプロバイダーは、フォームをアクティブ化せずに、フォームをクライアントに対して記述することができます。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapiform  <br/> |
|公開者:  <br/> |フォーム情報オブジェクト  <br/> |
|実装元:  <br/> |フォームライブラリプロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IMAPIFormInfo  <br/> |
|ポインターの種類:  <br/> |LPMAPIFORMINFO  <br/> |
|トランザクションモデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |フォームが使用するプロパティの完全なセットへのポインターを返します。  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |フォームが使用する動詞の完全なセットへのポインターを返します。  <br/> |
|[makeiconfrombinary](imapiforminfo-makeiconfrombinary.md) <br/> |フォームの icon プロパティからアイコンを作成します。  <br/> |
|[saveform](imapiforminfo-saveform.md) <br/> |構成ファイルに特定のフォームの説明を保存します。  <br/> |
|[openformcontainer](imapiforminfo-openformcontainer.md) <br/> |特定のフォームがインストールされているフォームコンテナーへのポインターを返します。  <br/> |
   
## <a name="remarks"></a>注釈

MapiForm ヘッダーファイルで定義されているほとんどのインターフェイスとは異なり、 **imapiforminfo**は imapiprop [:: GetProps](imapiprop-getprops.md)メソッドへの呼び出しを使用してほとんどのフォーム情報をエクスポートするため、imapiprop インターフェイスから継承します。 [](imapipropiunknown.md) 
  
## <a name="see-also"></a>関連項目



[MAPI のインターフェイス](mapi-interfaces.md)

