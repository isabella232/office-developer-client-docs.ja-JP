---
title: IPSTOVERRIDEREQ IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDEREQ
api_type:
- COM
ms.assetid: 22f497de-4afe-4433-965d-c3b5a66b05da
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7f3f6ae2b9849710bf44d3635fc7bb9a62016f48
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356981"
---
# <a name="ipstoverridereq--iunknown"></a>IPSTOVERRIDEREQ : IUnknown

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
個人用フォルダーファイル (PST) ストアプロバイダーのリソースにアクセスします。
  
|||
|:-----|:-----|
|継承元:  <br/> |IUnknown  <br/> |
|実装元:  <br/> |PST ストアプロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション  <br/> |
|インターフェイス識別子:  <br/> |IID_IPSTOVERRIDEREQ  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[IPSTOVERRIDEREQ::RegisterTrustedPSTOverrideHandler](ipstoverridereq-registertrustedpstoverridehandler.md) <br/> |個人用フォルダー (.pst) ファイルのロック解除手順を開始します。  <br/> |
   
## <a name="remarks"></a>解説

現在使用しているダウンロード可能なヘッダーファイルでは、PST オーバーライドハンドラインターフェイス識別子が定義されていない場合があります。その場合は、 [MAPI の定数](mapi-constants.md)のトピックに記載されているので、それをコピーしてコードに追加できます。 Microsoft Windows Software Development Kit (SDK) ヘッダーファイル guiddef で定義されている DEFINE_GUID マクロを使用して、グローバル一意識別子 (GUID) シンボリック名を値に関連付けます。 
  
詳細については、「 [Outlook 2007 で PSTDisableGrow ポリシーをバイパスするように PST オーバーライドハンドラーを実装する方法](https://support.microsoft.com/kb/956070)」を参照してください。
  
## <a name="see-also"></a>関連項目



[IPSTOVERRIDE1 : IUnknown](ipstoverride1iunknown.md)

