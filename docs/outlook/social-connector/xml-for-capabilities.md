---
title: 機能の XML
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: (.osc) プロバイダ XML スキーマの capabilities 要素を使用すると、.osc プロバイダーはその機能を指定できます。 そのような機能は次のとおりです。
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435006"
---
# <a name="xml-for-capabilities"></a>機能の XML

(.osc) プロバイダ XML スキーマの**capabilities**要素を使用すると、.osc プロバイダーはその機能を指定できます。 そのような機能は次のとおりです。 
  
- プロバイダーがソーシャルネットワークからのフレンドやアクティビティを取得、キャッシュ、または動的に検索することをサポートしているかどうか。
    
- .osc で特定のログオンユーザーインターフェイスを表示する方法。
    
- .osc がフォームベース認証を使用するか、ソーシャルネットワーク上のユーザーに対してソーシャルネットワークとログを自動的に構成するか。
    
**機能**の XML スキーマは、プロバイダーによってサポートされている機能を詳細に示すために重要です。 .osc プロバイダーは、_結果_の文字列を返す[imethod alprovider:: getcapabilities](isocialprovider-getcapabilities.md)メソッドを実装する必要があります。 .osc は**iな alprovider:: getcapabilities**を呼び出して、_結果_文字列の .osc プロバイダーの機能に関する情報を取得します。これは、 **capabilities**要素の XML スキーマ定義に準拠しています。 この情報によって、.osc から .osc プロバイダーへの後続の呼び出しが正しく動作するようになります。 
  
.osc プロバイダーの機能を**imethod alprovider:: getcapabilities**メソッドの出力パラメーターとして指定するには、.osc プロバイダ拡張 XML スキーマに準拠している必要があります。 次の図は、**機能**の XML データ構造を示しています。 
  
**図1。\<機能\> XML データ構造**

![機能 XML の構造](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
**capabilities**要素の子要素の詳細については、「[機能 XML 要素](capabilities-xml-elements.md)」を参照してください。 **機能**xml の例については、「 [capabilities xml の例](capabilities-xml-example.md)」を参照してください。 必要な要素やオプションの要素を含む、.osc プロバイダ XML スキーマの完全な定義については、「 [Outlook Social Connector プロバイダーの xml スキーマ](outlook-social-connector-provider-xml-schema.md)」を参照してください。
  
## <a name="see-also"></a>関連項目

- [機能 XML の例](capabilities-xml-example.md)  
- [フレンドとアクティビティの同期](synchronizing-friends-and-activities.md)  
- [Friends の XML](xml-for-friends.md)  
- [アクティビティの XML](xml-for-activities.md)
- [.osc XML スキーマを使用してプロバイダーを開発する](developing-a-provider-with-the-osc-xml-schema.md)

