---
title: iOS アプリケーションからの Office との統合
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office for iOS は、サード パーティ アプリケーションとの統合を可能にする拡張可能なソリューションを提供します。この記事では、アプリケーションから Office にユーザーを渡し、その後アプリケーションに戻すことによって、iOS アプリケーションから Office と統合する方法について説明します。
ms.openlocfilehash: d17a096c17eadab0cd94ee1dce18e979e80fa65d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299749"
---
# <a name="integrate-with-office-from-ios-applications"></a>iOS アプリケーションからの Office との統合

Office for iOS は、サード パーティ アプリケーションとの統合を可能にする拡張可能なソリューションを提供します。この記事では、アプリケーションから Office にユーザーを渡し、その後アプリケーションに戻すことによって、iOS アプリケーションから Office と統合する方法について説明します。
  
iOS デバイス上で Office を実行しているユーザーが、SharePoint または OneDrive に保存されているファイルを、任意のアプリケーションから開いて編集し、編集が完了したらすばやく元のアプリケーションに戻れるようにできます。そうするには、プロトコル ハンドラーを介してファイルを Office に渡し、Office で認識されるよう Office が確実に呼び出されるようにします。
  
Office アプリケーションの起動時に特定の情報を渡しておけば、ユーザーが編集を完了した際、Office アプリケーションの [戻る] 矢印を使ってドキュメントを閉じて元のストレージ アプリケーションに戻るようにすることができます。
  
## <a name="verify-that-office-has-been-installed"></a>Office がインストールされていることを確認する

参照元のアプリケーションは、最初に特定の Office アプリケーションがインストールされていることを確認する必要があります。次の Office アプリケーションは、ドキュメントを表示および編集するために iOS デバイスにインストールできます。
  
- Excel
    
- OneNote
    
- PowerPoint
    
- Word
    
[canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) メソッドを使用して、アプリケーションがリソースを開くことができるかどうかを確認します。このメソッドは、リソースの URL をパラメーターとして認識し、その URL を受け付けるアプリケーションを使用できない場合は **No** を返します。 **canOpenURL** が **No** を返す場合は、Office をインストールするようユーザーに要求する必要があります。
  
### <a name="prompt-the-user-to-install-office"></a>Office をインストールするようユーザーに求める

 特定の Office アプリケーションがインストールされていない場合は、[SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) オブジェクトを使用して iTunes アプリ ストアをアプリケーション内でレンダリングし、ユーザーにインストールする Office アプリケーションを示します。次の表に、ストア キット製品ビュー コントローラー内でそれぞれの Office アプリケーションを呼び出すための iTunes 識別子を一覧表示します。 
  
|**Office アプリケーション**|**iTunes 識別子**|
|:-----|:-----|
|Excel  <br/> |[https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|OneNote (iPhone)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|PowerPoint  <br/> |[https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|Word  <br/> |[https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a>Office を呼び出す

Office アプリケーションがインストールされている場合、参照元のアプリケーションは次の情報を渡すことで Office を呼び出すことができます。 
  
- Office プロトコル
    
- オープン モード
    
- URL
    
- Passback プロトコル
    
- ドキュメントのコンテキスト
    
スキーマ形式:
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
次の例は、編集用に Word ファイルを呼び出すための要求を示します。
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a>Office プロトコル

次の表に、各 Office アプリケーションのプロトコルを一覧表示します。 
  
|**アプリケーション**|**プロトコル**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|OneNote  <br/> |onenote:  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>オープン モード

Office アプリケーションは、ファイルを表示 (ofv) モードまたは編集 (ofe) モードで直接開くことができます。既定は編集モードです。 
  
スキーマ形式:
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL

URL は 3 つの部分で構成されます。 
  
- 編集用 (ofe) にファイルを開くための宣言
    
- URL 記述子 (|u|)
    
- URL
    
URL は、エンコードされる必要があり、ファイルへの直接リンク (リダイレクトではない) でなければなりません。URL が Office で扱うことのできない形式か、または単純にダウンロードに失敗した場合、Office は、呼び出し元のアプリケーションにユーザーを戻すことができません。 
  
スキーマ形式:
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a>Passback プロトコル (省略可能)

[戻る] 矢印をクリックしたときに Office がユーザーを iOS アプリケーションに戻るようにする場合、呼び出し元のアプリケーションは、Passback プロトコル (記述子 '|p|' (コロンなし) にアプリのプロトコルを続けたものを含む) を使用する必要があります。アプリケーションが Office からの応答を適切に処理できることを確認する必要があります。
  
スキーマ形式:
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a>ドキュメントのコンテキスト (省略可能)

Office はドキュメントのコンテキストを使用しませんが、Office がユーザーを戻すときに、参照元のアプリケーションが必要とする可能性があります。ドキュメントのコンテキストをアプリケーションに戻す場合は、記述子 '|c|' にコンテキストを続けて文字列として使用します。Office に文字列の長さの制限はありません。オペレーティング システムによって課される制限を超えることもできます。
  
スキーマ形式:
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a>参照元のアプリケーションにユーザーを返す

セキュリティ上の理由から、ファイルが正常に開いた場合、Office は参照元のアプリケーションにユーザーのみを返します。ユーザーが [戻る] 矢印をクリックすると、参照元のアプリケーションに対して Office は、Passback プロトコル、オープン モード、URL、アップロード保留中の状態、およびドキュメントのコンテキストで応答します。アップロード保留中の状態は、記述子 |z| を使用し、"yes" または "no" のいずれかです。
  
スキーマ形式:
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [canOpenURL メソッド](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [UIApplication クラス](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [SKProductViewController オブジェクト](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

