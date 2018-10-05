---
title: Android アプリケーションからの Office との統合
manager: soliver
ms.date: 06/18/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a765fa49-a272-4047-9147-59cc68e5dd27
description: Office for Android は、サード パーティのアプリケーションとの統合を可能にする、拡張可能なソリューションを提供します。Android アプリケーションから Office にユーザーを渡すことにより、そのアプリケーションから Office と統合できます。
ms.openlocfilehash: 4e674b3d66f3acba7e9c9c19e716ff0d73d803b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393027"
---
# <a name="integrate-with-office-from-android-applications"></a>Android アプリケーションからの Office との統合

Office for Android は、サード パーティのアプリケーションとの統合を可能にする、拡張可能なソリューションを提供します。Android アプリケーションから Office にユーザーを渡すことにより、そのアプリケーションから Office と統合できます。
  
Android デバイスで Office を実行しているユーザーが、SharePoint または OneDrive に保管されたファイルを、任意のアプリケーションから開いて編集できるようにすることができます。そのためには、プロトコル ハンドラーを通してファイルを Office に渡し、Office が理解できる方法で Office を呼び出します。
  
ユーザーは、ファイルの編集が終わったら、デバイスの戻るキーを選択して、元のストレージ アプリケーションに戻ることができます。
  
## <a name="verify-that-office-has-been-installed"></a>Office がインストールされていることの確認

特定の Office アプリケーションがインストールされていることを、まず参照元のアプリケーションが確認します。文書の表示と編集用に以下の Office アプリケーションを Android デバイスにインストールできます。 
  
- Excel
    
- PowerPoint
    
- Word
    
特定の Office アプリケーションがインストールされているかどうかを判別するには、Android PackageManager を使用します。この処理で使用できる Office アプリケーションのパッケージ名を以下の表に一覧で示します。
  
|**アプリケーション**|**パッケージ名**|
|:-----|:-----|
|Excel  <br/> |com.microsoft.office.excel  <br/> |
|PowerPoint  <br/> |com.microsoft.office.powerpoint  <br/> |
|Word  <br/> |com.microsoft.office.word  <br/> |
   
### <a name="prompt-the-user-to-install-office"></a>Office をインストールするようユーザーにプロンプトを出す

特定の Office アプリケーションがインストールされていない場合、アプリケーションをインストールするようユーザーにプロンプトを出すことができます。以下の表に、Office アプリケーションの使用可能なインストール場所の一覧を示します。
  
|**アプリケーション**|**Google Play ストア**|
|:-----|:-----|
|Excel  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.excel](https://play.google.com/store/apps/details?id=com.microsoft.office.excel) <br/> |
|PowerPoint  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint](https://play.google.com/store/apps/details?id=com.microsoft.office.powerpoint) <br/> |
|Word  <br/> |[https://play.google.com/store/apps/details?id=com.microsoft.office.word](https://play.google.com/store/apps/details?id=com.microsoft.office.word) <br/> |
   
## <a name="invoke-office"></a>Office を呼び出す

Office アプリケーションがインストールされている場合、参照元のアプリケーションは次の情報を渡すことで Office を呼び出すことができます。
  
- Office プロトコル
    
- オープン モード
    
- URL
    
スキーマ形式:
  
 `<Office protocol><open mode>|u|<URL>`
  
Word ファイルを編集用に呼び出す要求の例を以下に示します。
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx`
  
### <a name="office-protocols"></a>Office プロトコル

次の表に、各 Office アプリケーションのプロトコルを一覧表示します。
  
|**アプリケーション**|**プロトコル**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
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
  
## <a name="see-also"></a>関連項目
<a name="bk_addresources"> </a>

- [Office との統合](integrate-with-office.md)
    
- [PackageManager](https://developer.android.com/reference/android/content/pm/PackageManager.html)
    
- [GetPackageManager()](https://developer.android.com/reference/android/content/Context.html)
    

