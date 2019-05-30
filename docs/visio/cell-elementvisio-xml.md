---
title: Cell 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3131bfbb-9bf6-d15d-c6ca-2f15bd038f39
description: DocumentSheet、StyleSheet、PageSheet、またはシェイプシート内に含めることができる cell 要素を指定します。
ms.openlocfilehash: 2b76abeb83fb7251bf492e92d8dd1a81feeab092
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542311"
---
# <a name="cell-element-visio-xml"></a>Cell 要素 (Visio XML)

DocumentSheet、StyleSheet、PageSheet、またはシェイプシート内に含めることができる cell 要素を指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書 .xml、system.xml、masters、.master、マスター # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell"  type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |図形の定義に関する情報を提供する cell 要素を指定します。  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |DocumentSheet の構造を定義します。  <br/> |
|[Xsl](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |図面で定義されているスタイルを表します。  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |マスターシェイプに関連付けられている図面ページのプロパティを指定します。  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |図面ページに関連付けられた図面ページのプロパティを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: string  <br/> |省略可能  <br/> |数式がエラーとして評価されることを示します。 **E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラーメッセージ文字列。  <br/> |
|F  <br/> |xsd: string  <br/> |省略可能  <br/> | 要素の数式を表します。 この属性には、次のいずれかの文字列を含めることができます。  <br/>  ' (一部の数式) ' (数式がローカルに存在する場合)  <br/>  `No Formula`数式がローカルで削除またはブロックされている場合  <br/>  `Inh`数式が継承されている場合。  <br/> |数式。  <br/> |
|N  <br/> |xsd: string  <br/> |必須  <br/> |**シェイプシート**セルの名前を表します。  <br/> |**シェイプシート**セルの名前を指定します。  <br/> 下記の「備考」を参照してください。  <br/> |
|U  <br/> |xsd: string  <br/> |省略可能  <br/> |既定値は DL である計量単位を表します。  <br/> |セルの単位を示します。  <br/> |
|V  <br/> |xsd: string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |**シェイプシート**セルの値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。 この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|[Addmarkup]  <br/> |図面が校正履歴用にチェックされているかどうかを示します。  <br/> |[[AddMarkup] セル ([Document Properties] セクション)](addmarkup-cell-document-properties-section.md) <br/> |
|Alignbottom]  <br/> |親図形の原点を基準として、図形の下部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。  <br/> |[[AlignBottom] セル ([Alignment] セクション)](alignbottom-cell-alignment-section.md) <br/> |
|[Aligncenter]  <br/> |親図形の原点を基準として、図形の水平方向の中心を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。  <br/> |[[AlignCenter] セル ([Alignment] セクション)](aligncenter-cell-alignment-section.md) <br/> |
|[Alignleft]  <br/> |親図形の原点を基準として、図形の左辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。  <br/> |[[AlignLeft] セル ([Alignment] セクション)](alignleft-cell-alignment-section.md) <br/> |
|[Alignmiddle]  <br/> |親図形の原点を基準として、図形の垂直方向の中心を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。  <br/> |[[AlignMiddle] セル ([Alignment] セクション)](alignmiddle-cell-alignment-section.md) <br/> |
|[Alignright]  <br/> |親図形の原点を基準として、図形の右辺を揃えるための垂直ガイドまたはガイド点の水平方向の位置を指定します。  <br/> |[[AlignRight] セル ([Alignment] セクション)](alignright-cell-alignment-section.md) <br/> |
|AlignTop  <br/> |親図形の原点を基準として、図形の上部の辺を揃えるための水平ガイドまたはガイド点の垂直方向の位置を指定します。  <br/> |[[AlignTop] セル ([Alignment] セクション)](aligntop-cell-alignment-section.md) <br/> |
|角度  <br/> |親図形を基準としたときの、図形の現在の回転角度を表します。1-D 図形の回転角度を決定する既定の数式は =ATAN2(EndY-BeginY,EndX-BeginX) です。  <br/> |[[Angle] セル ([Shape Transform] セクション)](angle-cell-shape-transform-section.md) <br/> |
|[Avenuesizex]  <br/> |[レイアウトの構成] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の水平方向の間隔を指定します ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。  <br/> |[[AvenueSizeX] セル ([Page Layout] セクション)](avenuesizex-cell-page-layout-section.md) <br/> |
|[Avenuesizey]  <br/> |[レイアウトの構成] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の垂直方向の間隔を指定します ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。 [レイアウトの構成] ダイアログボックスを使用して図形をレイアウトするときの、図面ページ上の図形の垂直方向の間隔を指定します ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。  <br/> |[[AvenueSizeY] セル ([Page Layout] セクション)](avenuesizey-cell-page-layout-section.md) <br/> |
|AvoidPageBreaks  <br/> |図形を整列するか、均等に配置するか、またはその両方を行う場合に、図形を改ページの上に配置できるかどうかを指定します。  <br/> |[[Avoidpagebreaks] セル (ページレイアウトセクション)](avoidpagebreaks-cell-page-layout-section.md) <br/> |
|Beginarrow]  <br/> |線の最初の頂点に、矢印またはその他の線の端点の書式があるかどうかを示します。 0 ~ 45 の数値、またはユーザー設定の線の端点の名前を使用する関数を入力するか、[線] ダイアログボックスを使用します。  <br/> |[[BeginArrow] セル ([Line Format] セクション)](beginarrow-cell-line-format-section.md) <br/> |
|[Beginarrowsize]  <br/> |線の開始位置にある矢印のサイズを指定します。  <br/> |[[BeginArrowSiz] セル ([Line Format] セクション)](beginarrowsize-cell-line-format-section.md) <br/> |
|BeginX  <br/> |親図形の原点を基準としたときの 1 次元図形の始点の x 座標を表します。 親図形の原点を基準としたときの 1 次元図形の始点の x 座標を表します。  <br/> |[[BeginX] セル ([1-D Endpoints] セクション)](beginx-cell-1-d-endpoints-section.md) <br/> |
|BeginY  <br/> |親図形の原点を基準としたときの 1-D 図形の始点の y 座標を表します。  <br/> |[[BeginY] セル ([1-D Endpoints] セクション)](beginy-cell-1-d-endpoints-section.md) <br/> |
|[Begtrigger]  <br/> |アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の始点を移動するときに別の図形に対する接続を維持するかどうかを指定します。  <br/> |[[BegTrigger] セル ([Glue Info] セクション)](begtrigger-cell-glue-info-section.md) <br/> |
|[Bevelbottomheight]  <br/> |図形の下面取りの高さをポイント単位で指定します。  <br/> |[斜めの高さセル (面取りのプロパティセクション)](bevelbottomheight-cell-bevel-properties-section.md) <br/> |
|BevelBottomType  <br/> |図形の面取りの下面取りの種類を指定します。  <br/> |[傾斜 El下の種類のセル (面取りのプロパティ] セクション)](bevelbottomtype-cell-bevel-properties-section.md) <br/> |
|[Bevelbottomwidth]  <br/> |下面取りの幅をポイント単位で指定します。  <br/> |[[傾斜] [幅] セル ([面取りのプロパティ] セクション)](bevelbottomwidth-cell-bevel-properties-section.md) <br/> |
|[Bevelcontourcolor]  <br/> |面取りの輪郭の色を RGB 値で指定します。または、アクティブなテーマによって決定されます。  <br/> |[傾斜 Elクレヨンの Color セル (面取りのプロパティセクション)](bevelcontourcolor-cell-bevel-properties-section.md) <br/> |
|[Bevelcontoursize]  <br/> |面取りの輪郭のサイズをポイント単位で指定します。  <br/> |[「斜め Elクレヨン Oursize」セル (ベベルのプロパティ) セクション](bevelcontoursize-cell-bevel-properties-section.md) <br/> |
|[Beveldepthcolor]  <br/> |ベベルの奥行きの色を RGB 値で指定します。または、アクティブなテーマによって決定されます。  <br/> |[[Beveldepthcolor] セル (面取りのプロパティ] セクション)](beveldepthcolor-cell-bevel-properties-section.md) <br/> |
|[Beveldepthsize]  <br/> |面取りの奥行きのサイズをポイント単位で指定します。  <br/> |[[Beveldepthsize] セル (面取りのプロパティ] セクション)](beveldepthsize-cell-bevel-properties-section.md) <br/> |
|[Bevellightingangle]  <br/> |角度 (°) の角度を指定します。  <br/> |[[Bevellightingangle] セル (面取りのプロパティ] セクション)](bevellightingangle-cell-bevel-properties-section.md) <br/> |
|[Bevellightingtype]  <br/> |ベベル効果に使用する光源の種類を決定します。  <br/> |[[Bevellightingtype] セル (面取りのプロパティ] セクション)](bevellightingtype-cell-bevel-properties-section.md) <br/> |
|[Bevelmaterialtype]  <br/> |ベベルを構成する素材の種類を指定します。  <br/> |[[Bevelmaterialtype] セル (面取りのプロパティ] セクション)](bevelmaterialtype-cell-bevel-properties-section.md) <br/> |
|[Beveltopheight]  <br/> |図形の上面取りの高さをポイント単位で指定します。  <br/> |[斜めの高さセル (面取りのプロパティセクション)](beveltopheight-cell-bevel-properties-section.md) <br/> |
|BevelTopType  <br/> |図形の上端にあるベベルの種類を指定します。  <br/> |[BevelTopType セル (面取りのプロパティ] セクション)](beveltoptype-cell-bevel-properties-section.md) <br/> |
|[Beveltopwidth]  <br/> |上面取りの幅をポイント単位で指定します。  <br/> |[[額縁 Eltopwidth] セル ([面取りのプロパティ] セクション)](beveltopwidth-cell-bevel-properties-section.md) <br/> |
|[Blocksizex]  <br/> |[レイアウトの構成] ダイアログボックスを使用して図形をレイアウトするときに、図形が図面ページ上に収まっている領域を、水平方向のブロックサイズを指定します。  <br/> |[[BlockSizeX] セル ([Page Layout] セクション)](blocksizex-cell-page-layout-section.md) <br/> |
|[Blocksizey]  <br/> |[レイアウトの構成] ダイアログを使用して図形をレイアウトするときに、それぞれの図形が図面ページに収まっている必要がある領域を、垂直方向のブロックサイズを指定します。  <br/> |[[BlockSizeY] セル ([Page Layout] セクション)](blocksizey-cell-page-layout-section.md) <br/> |
|Blur  <br/> |ビットマップ イメージをぼかしたり、色をやわらげたりします。 既定値は 0% です。  <br/> |[[Blur] セル ([Image Properties] セクション)](blur-cell-image-properties-section.md) <br/> |
|BottomMargin  <br/> |テキスト ブロックの下の枠線からそのテキスト ブロックに含まれるテキストの最終行までの距離を指定します。  <br/> |[[BottomMargin] セル ([Text Block Format] セクション)](bottommargin-cell-text-block-format-section.md) <br/> |
|Brightness  <br/> |ビットマップイメージの明るさを調整します。  <br/> |[輝度セル (Image Properties セクション](brightness-cell-image-properties-section.md) <br/> |
|カレンダー  <br/> |セル数式が Date 情報を含むときに使用するカレンダーを指定します。  <br/> |[[Calendar] セル ([Miscellaneous] セクション)](calendar-cell-miscellaneous-section.md) <br/> |
|カレンダー  <br/> |データ型が Date のときに図形データに使用するカレンダーを指定します。  <br/> |[[Calendar] セル ([Shape Data] セクション)](calendar-cell-shape-data-section.md) <br/> |
|カレンダー  <br/> |データ型が Date のときに、テキストフィールドに使用するカレンダーを指定します。  <br/> |[[Calendar] セル ([Text Fields] セクション)](calendar-cell-text-fields-section.md) <br/> |
|[Centerx]  <br/> |図面ページをプリンター ページの左右の中央に揃えるかどうかを指定します。  <br/> |[[CenterX] セル ([Print Properties] セクション)](centerx-cell-print-properties-section.md) <br/> |
|[Centery]  <br/> |図面ページをプリンター ページの上下の中央に揃えるかどうかを指定します。  <br/> |[[CenterY] セル ([Print Properties] セクション)](centery-cell-print-properties-section.md) <br/> |
|[Clippingpath]  <br/> |イメージを限定しているパスの図形座標への参照を格納します。  <br/> |[[Clippingpath] セル (外部イメージ情報セクション)](clippingpath-cell-foreign-image-info-section.md) <br/> |
|[Colorschemeindex]  <br/> |図形に適用されるテーマの配色を整数で指定します。  <br/> |[[Colorschemeindex] セル (テーマのプロパティセクション)](colorschemeindex-cell-theme-properties-section.md) <br/> |
|Comment  <br/> |コメント内に表示されるテキストが含まれます。  <br/> |[[Comment] セル ([Annotation] セクション)](comment-cell-annotation-section.md) <br/> |
|Comment  <br/> |図形のコメント テキストを文字列形式で格納します。  <br/> |[[Comment] セル ([Miscellaneous] セクション)](comment-cell-miscellaneous-section.md) <br/> |
|[Compoundtype]  <br/> |図形の線の複合型を指定します。  <br/> |[[[Compoundtype] セル ([Line Format] セクション)](compoundtype-cell-line-format-section.md) <br/> |
|[Confixedcode]  <br/> |コネクタの経路の変更方法を指定します。  <br/> |[[ConFixedCode] セル ([Shape Layout] セクション)](confixedcode-cell-shape-layout-section.md) <br/> |
|[Conlinejumpcode]  <br/> |コネクタの飛び越し点の表示方法を指定します。  <br/> |[[ConLineJumpCode] セル ([Shape Layout] セクション)](conlinejumpcode-cell-shape-layout-section.md) <br/> |
|[Conlinejumpdirx]  <br/> |図形に接続する水平方向の動的コネクタに表示される飛び越し点の向きを指定します。  <br/> |[[ConLineJumpDirX] セル ([Shape Layout] セクション)](conlinejumpdirx-cell-shape-layout-section.md) <br/> |
|[Conlinejumpdiry]  <br/> |図形に接続する垂直方向の動的コネクタに表示される飛び越し点の向きを指定します。  <br/> |[[ConLineJumpDirY] セル ([Shape Layout] セクション)](conlinejumpdiry-cell-shape-layout-section.md) <br/> |
|[Conlinejumpstyle]  <br/> |動的コネクタの飛び越し点のスタイルを指定します。  <br/> |[[ConLineJumpStyle] セル ([Shape Layout] セクション)](conlinejumpstyle-cell-shape-layout-section.md) <br/> |
|[Conlinerouteext]  <br/> |コネクタの外観を指定します。  <br/> |[[ConLineRouteExt] セル ([Shape Layout] セクション)](conlinerouteext-cell-shape-layout-section.md) <br/> |
|[Connectorschemeindex]  <br/> |図形に適用されるテーマのコネクタスキームを整数で指定します。  <br/> |[[Connectorschemeindex] セル (テーマのプロパティセクション)](connectorschemeindex-cell-theme-properties-section.md) <br/> |
|Contrast  <br/> |ビットマップイメージのコントラストを調整します。  <br/> |[[Contrast] セル ([Image Properties] セクション)](contrast-cell-image-properties-section.md) <br/> |
|著作権  <br/> |ユーザーが判読できる著作権ステートメントを表す文字列を格納します。  <br/> ||
|[Ctrlasinput]  <br/> |コントロール ハンドルを使用して図形を操作するときに、どの図形を親図形にするかを指定します。このセルの値は、図面ページ上にあるすべての図形の動作に適用されます。  <br/> |[[CtrlAsInput] セル ([Page Layout] セクション)](ctrlasinput-cell-page-layout-section.md) <br/> |
|DefaultTabStop  <br/> |テキスト ブロックの既定のタブ位置の間隔を指定します。  <br/> |[[DefaultTabstop] セル ([Text Block Format] セクション)](defaulttabstop-cell-text-block-format-section.md) <br/> |
|[Denoise]  <br/> |ビットマップイメージからノイズ (ランダムに分散した色レベルのピクセル) を削除します。  <br/> |[[Denoise] セル ([Image Properties] セクション)](denoise-cell-image-properties-section.md) <br/> |
|DisplayLevel  <br/> |図形の表示レベル バンド (Z オーダー グループ化の相対範囲) を指定します。  <br/> |[DisplayLevel セル (Shape Layout セクション)](displaylevel-cell-shape-layout-section.md) <br/> |
|DisplayMode  <br/> |グループ図形とそのメンバーの表示方法を指定します。  <br/> |[[DisplayMode] セル ([Group Properties] セクション)](displaymode-cell-group-properties-section.md) <br/> |
|DisplayMode  <br/> |ユーザーがタグの上にポインターを移動したとき、図形を選択したとき、または常に [アクション] タグを表示するかどうかを指定します。  <br/> |[[DisplayMode] セル ([Smart Tags] セクション)](displaymode-cell-action-tags-section.md) <br/> |
|[Distancefromground]  <br/> |3-d で回転したときに、オブジェクトが地上からポイント単位で発生する距離を指定します。  <br/> |[[DistanceFromGround] セル ([3-D 回転のプロパティ] セクション)](distancefromground-cell-3-d-rotation-properties.md) <br/> |
|[Doclangid]  <br/> |図面の既定の言語を示します。  <br/> |[[DocLangID] セル ([Document Properties] セクション)](doclangid-cell-document-properties-section.md) <br/> |
|[Doclockduplicatepage]  <br/> |ドキュメントのページを複製できるかどうかを、ブール演算型で決定します。  <br/> |[[Doclockduplicatepage] セル (ドキュメントのプロパティ] セクション)](doclockduplicatepage-cell-document-properties-section.md) <br/> |
|[Doclockreplace]  <br/> |置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。  <br/> |[[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)](doclockreplace-cell-document-properties-section.md) <br/> |
|[Dontmovechildren]  <br/> |グループ内の図形をマウスを使用してドラッグできるかどうかを指定します。  <br/> |[[DontMoveChildren] セル ([Group Properties] セクション)](dontmovechildren-cell-group-properties-section.md) <br/> |
|[Drawingresizetype]  <br/> |図面ページのサイズをダイアグラムに合わせて自動的に変更するかどうかを指定します。  <br/> |[[Drawingresizetype] セル (ページのプロパティ] セクション)](drawingresizetype-cell-page-properties-section.md) <br/> |
|Drawingscale]  <br/> |現在の図面縮尺で、図面単位の値を表します。  <br/> |[[DrawingScale] セル ([Page Properties] セクション)](drawingscale-cell-page-properties-section.md) <br/> |
|[Drawingscaletype]  <br/> |[ページ設定] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[ホーム] タブで [ページ設定] 矢印をクリックします)。  <br/> |[[DrawingScaleType] セル ([Page Properties] セクション)](drawingscaletype-cell-page-properties-section.md) <br/> |
|[Drawingsizetype]  <br/> |図面のサイズを指定します。  <br/> |[[DrawingSizeType] セル ([Page Properties] セクション)](drawingsizetype-cell-page-properties-section.md) <br/> |
|[Droponpagescale]  <br/> |図形を図面ページにドロップしたときの縮尺のパーセント値が含まれます。  <br/> |[[DropOnPageScale] セル ([Miscellaneous] セクション)](droponpagescale-cell-miscellaneous-section.md) <br/> |
|[Dynamicsoff]  <br/> |図面ページ上にある他の図形やコネクタに合わせて、配置可能な図形を移動したり、コネクタを迂回させるかどうかを指定します。  <br/> |[[DynamicsOff] セル ([Page Layout] セクション)](dynamicsoff-cell-page-layout-section.md) <br/> |
|[Dynfeedback]  <br/> |コネクタをドラッグしたときにユーザーに対して表示されるフィードバックの種類を変更します。  <br/> |[[DynFeedback] セル ([Miscellaneous] セクション)](dynfeedback-cell-miscellaneous-section.md) <br/> |
|[Effectschemeindex]  <br/> |図形に適用されるテーマの効果設定を整数で指定します。  <br/> |[[Effectschemeindex] セル (テーマのプロパティセクション)](effectschemeindex-cell-theme-properties-section.md) <br/> |
|[Embellishmentindex]  <br/> |吹き出し、コンテナー、タイムライン、および組織図の図形の外観 (装飾記号) を変更します。  <br/> |[[Embellishmentindex] セル (テーマのプロパティセクション)](embellishmentindex-cell-theme-properties-section.md) <br/> |
|[Enablefillprops]  <br/> |スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。  <br/> |[[EnableFillProps] セル ([Style Properties] セクション)](enablefillprops-cell-style-properties-section.md) <br/> |
|[Enablegrid]  <br/> |[レイアウトの構成] ダイアログボックスでレイアウトを構成するときに、表示されていない内部のページグリッドに基づいて、アプリケーションで図形をレイアウトするかどうかを指定します。  <br/> |[[EnableGrid] セル ([Page Layout] セクション)](enablegrid-cell-page-layout-section.md) <br/> |
|[Enablelineprops]  <br/> |スタイルに線のプロパティを含めるかどうかを指定します。  <br/> |[[EnableLineProps] セル ([Style Properties] セクション)](enablelineprops-cell-style-properties-section.md) <br/> |
|[Enabletextprops]  <br/> |スタイルにテキストのプロパティを含めるかどうかを指定します。  <br/> |[[EnableTextProps] セル ([Style Properties] セクション)](enabletextprops-cell-style-properties-section.md) <br/> |
|[Endarrow]  <br/> |線の最後の頂点に対して、矢印を付けるか、または別の書式の端点を適用するかを指定します。  <br/> |[[EndArrow] セル ([Line Format] セクション)](endarrow-cell-line-format-section.md) <br/> |
|[Endarrowsize]  <br/> |線の終端にある矢印のサイズを指定します。  <br/> |[[EndArrowSize] セル ([Line Format] セクション)](endarrowsize-cell-line-format-section.md) <br/> |
|[Endtrigger]  <br/> |アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の終点を移動するときに別の図形に対する接続を維持するかどうかを指定します。  <br/> |[[EndTrigger] セル ([Glue Info] セクション)](endtrigger-cell-glue-info-section.md) <br/> |
|EndX  <br/> |親図形の原点を基準としたときの、1-D 図形の終点の x 座標を表します。  <br/> |[[EndX] セル ([1-D Endpoints] セクション)](endx-cell-1-d-endpoints-section.md) <br/> |
|EndY  <br/> |親図形の原点を基準としたときの、1-D 図形の終点の y 座標を表します。  <br/> |[[EndY] セル ([1-D Endpoints] セクション)](endy-cell-1-d-endpoints-section.md) <br/> |
|Eventdblclick]  <br/> |図形をダブルクリックしたときに評価されるイベント セルです。  <br/> |[[EventDblClick] セル ([Events] セクション)](eventdblclick-cell-events-section.md) <br/> |
|[Eventdrop]  <br/> |図面ページに図形をインスタンスとしてドロップしたとき、または図形を複製したり貼り付けたときに評価されるイベント セルです。  <br/> |[[EventDrop] セル ([Events] セクション)](eventdrop-cell-events-section.md) <br/> |
|[Eventmultidrop]  <br/> |図面ページに複数の図形をインスタンスとしてドロップしたとき、または図形を複製または貼り付けたときに評価されるイベントセルです。  <br/> |[EventMultiDrop ドロップセル (Events セクション)](eventmultidrop-cell-events-section.md) <br/> |
|[Eventxfmod]  <br/> |ページ上で、図形の位置または向きの変更 ("XF") が行われたときに評価されるイベント セルです。  <br/> |[[EventXFMod] セル ([Events] セクション)](eventxfmod-cell-events-section.md) <br/> |
|[Fillbkgnd]  <br/> |図形の塗りつぶしのパターンで背景に使用する色 (塗りつぶし部分) を指定します。  <br/> |[[FillBkgnd] セル ([Fill Format] セクション)](fillbkgnd-cell-fill-format-section.md) <br/> |
|[Fillbkgndtrans]  <br/> |図形の塗りつぶしのパターンに対して、背景 (塗りつぶし部分) に適用される透過性レベルを指定します。  <br/> |[[FillBkgndTrans] セル ([Fill Format] セクション)](fillbkgndtrans-cell-fill-format-section.md) <br/> |
|[Fillforegnd]  <br/> |図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。  <br/> |[[FillForegnd] セル ([Fill Format] セクション)](fillforegnd-cell-fill-format-section.md) <br/> |
|[Fillforegndtrans]  <br/> |図形の塗りつぶしのパターンに対して、背景 (塗りつぶし部分) に適用される透過性レベルを指定します。  <br/> |[[FillForegndTrans] セル ([Fill Format] セクション)](fillforegndtrans-cell-fill-format-section.md) <br/> |
|[Fillgradientangle]  <br/> |線形の方向を使用して、グラデーションの塗りつぶしのグラデーションの角度を指定します。  <br/> |[[Fillgradientangle] セル (グラデーションのプロパティ] セクション)](fillgradientangle-cell-gradient-properties-section.md) <br/> |
|[Fillgradientdir]  <br/> |塗りつぶしのグラデーションの方向を決定します。 グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。  <br/> |[[Fillgradientdir] セル (グラデーションのプロパティ] セクション)](fillgradientdir-cell-gradient-properties-section.md) <br/> |
|[Fillgradientenabled]  <br/> |この図形で塗りつぶしのグラデーションを有効にするかどうかを決定します。  <br/> |[[Fillgradientenabled] セル (グラデーションのプロパティ] セクション)](fillgradientenabled-cell-gradient-properties-section.md) <br/> |
|Fillpattern]  <br/> |図形の塗りつぶしのパターンを指定します。 ユーザー設定の塗りつぶしのパターンを指定するには、このセルで USE 関数を使用します。  <br/> |[[FillPattern] セル ([Fill Format] セクション)](fillpattern-cell-fill-format-section.md) <br/> |
|[Flipx]  <br/> |図形が左右反転されているかを示します。  <br/> |[[FlipX] セル ([Shape Transform] セクション)](flipx-cell-shape-transform-section.md) <br/> |
|[Flipy]  <br/> |図形が上下反転されているかを示します。  <br/> |[[FlipY] セル ([Shape Transform] セクション)](flipy-cell-shape-transform-section.md) <br/> |
|[Fontschemeindex]  <br/> |図形に適用するテーマのフォントパターンを整数で指定します。  <br/> |[[Fontschemeindex] セル (テーマのプロパティセクション](fontschemeindex-cell-theme-properties-section.md) <br/> |
|Gamma  <br/> |モニターやスキャナーなど、特定の出力装置に合わせてイメージの明暗度の強さを調整または補正します。既定値は 1 (補正なし) です。  <br/> |[[Gamma] セル ([Image Properties] セクション)](gamma-cell-image-properties-section.md) <br/> |
|[Glowcolor]  <br/> |図形に適用する外側のグローのストロークに使用する色を、RGB またはテーマの値で決定します。  <br/> |[[Glowcolor] セル (その他の効果のプロパティセクション)](glowcolor-cell-additional-effect-properties-section.md) <br/> |
|[Glowcolortrans]  <br/> |図形の光彩のストロークに使用する色の透過性レベルをパーセンテージで指定します。  <br/> |[[Glowcolortrans] セル (その他の効果のプロパティセクション)](glowcolortrans-cell-additional-effect-properties-section.md) <br/> |
|[Glowsize]  <br/> |図形の外側の光彩のサイズをポイント単位で指定します。  <br/> |[[Glowsize] セル (その他の効果のプロパティセクション)](glowsize-cell-additional-effect-properties-section.md) <br/> |
|[Gluetype]  <br/> |1-D 図形を別の図形に接着するときに静的接着 (点から点) と動的接着 (図形から図形) のどちらを使用するかを指定します。  <br/> |[[GlueType] セル ([Glue Info] セクション)](gluetype-cell-glue-info-section.md) <br/> |
|Height  <br/> |図形の高さを図面単位で指定します。  <br/> |[[Height] セル ([Shape Transform] セクション)](height-cell-shape-transform-section.md) <br/> |
|HelpTopic  <br/> |図形のヘルプトピック ID を指定します。  <br/> ||
|[Hideforapply]  <br/> |Microsoft Visio ユーザーインターフェイスでスタイルが表示されている場所を決定します。  <br/> |[[HideForApply] セル ([Style Properties] セクション)](hideforapply-cell-style-properties-section.md) <br/> |
|[Hidetext]  <br/> |図形のテキストを非表示にします。  <br/> |[[HideText] セル ([Miscellaneous] セクション)](hidetext-cell-miscellaneous-section.md) <br/> |
|[Imgheight]  <br/> |枠内におけるオブジェクトのイメージの高さを指定します。  <br/> |[[ImgHeight] セル ([Foreign Image Info] セクション)](imgheight-cell-foreign-image-info-section.md) <br/> |
|[Imgoffsetx]  <br/> |オブジェクトの枠の原点からオブジェクトを水平方向へオフセットする距離を指定します。  <br/> |[[ImgOffsetX] セル ([Foreign Image Info] セクション)](imgoffsetx-cell-foreign-image-info-section.md) <br/> |
|[Imgoffsety]  <br/> |オブジェクトの枠の原点からオブジェクトを垂直方向へオフセットする距離を指定します。  <br/> |[[ImgOffsetY] セル ([Foreign Image Info] セクション)](imgoffsety-cell-foreign-image-info-section.md) <br/> |
|[Imgwidth]  <br/> |枠内におけるオブジェクトのイメージの幅を指定します。  <br/> |[[ImgWidth] セル ([Foreign Image Info] セクション)](imgwidth-cell-foreign-image-info-section.md) <br/> |
|[Inhibitsnap]  <br/> |前景ページ上の図形を、同じページにある他のオブジェクトや背景ページ上の図形にスナップするかどうかを指定します。  <br/> |[[InhibitSnap] セル ([Page Properties] セクション)](inhibitsnap-cell-page-properties-section.md) <br/> |
|[Isdropsource]  <br/> |図形をドロップしてグループに追加できるかどうかを指定します。  <br/> |[[IsDropSource] セル ([Miscellaneous] セクション)](isdropsource-cell-miscellaneous-section.md) <br/> |
|[Isdroptarget]  <br/> |グループにドロップされた図形を、そのグループが受け入れるかどうかを決定します。  <br/> |[[IsDropTarget] セル ([Group Properties] セクション)](isdroptarget-cell-group-properties-section.md) <br/> |
|[Issnaptarget]  <br/> |グループにスナップするかグループ内の図形にスナップするかを指定します。  <br/> |[[IsSnapTarget] セル ([Group Properties] セクション)](issnaptarget-cell-group-properties-section.md) <br/> |
|[Istextedittarget]  <br/> |グループに対するテキストの割り当て方を指定します。  <br/> |[[IsTextEditTarget] セル ([Group Properties] セクション)](istextedittarget-cell-group-properties-section.md) <br/> |
|[Keeptextflat]  <br/> |図形のテキストが3-d 図形の回転を無視するかどうかを示します。 2-D 回転には適用されません。  <br/> |[KeepTextFlat セル (3-d 回転プロパティセクション)](keeptextflat-cell-3-d-rotation-properties-section.md) <br/> |
|LangID  <br/> |コメントの記入に使用した言語を示します。  <br/> |[[LangID] セル ([Annotation] セクション)](langid-cell-annotation-section.md) <br/> |
|LangID  <br/> |テキストの記入に使用した言語を示します。  <br/> |[[LangID] セル ([Character] セクション)](langid-cell-character-section.md) <br/> |
|LangID  <br/> |セル数式の作成に使用した言語を示します。  <br/> |[[LangID] セル ([Miscellaneous] セクション)](langid-cell-miscellaneous-section.md) <br/> |
|LangID  <br/> |図形データ値の記入に使用した言語を示します。  <br/> |[[LangID] セル ([Shape Data] セクション)](langid-cell-shape-data-section.md) <br/> |
|レイヤーメンバ  <br/> |ページの0から始まるレイヤーのインデックスに基づいて、図形の layer membership を指定します。 図形が複数のレイヤーに割り当てられている場合、各レイヤーインデックスはセミコロンで区切られて表示されます。  <br/> ||
|LeftMargin  <br/> |テキスト ブロックの左枠からそのブロックに含まれるテキストまでの距離を指定します。  <br/> |[[LeftMargin] セル ([Text Block Format] セクション)](leftmargin-cell-text-block-format-section.md) <br/> |
|[Lineadjustfrom]  <br/> |複数の動的コネクタが迂回する場合に、線を分離するコネクタを指定します。  <br/> |[[LineAdjustFrom] セル ([Page Layout] セクション)](lineadjustfrom-cell-page-layout-section.md) <br/> |
|[Lineadjustto]  <br/> |線を束ねるときに対象とする動的コネクタを指定します。  <br/> |[[LineAdjustTo] セル ([Page Layout] セクション)](lineadjustto-cell-page-layout-section.md) <br/> |
|[Linecap]  <br/> |線の端点を丸、四角形、または拡張のどれにするかを指定します。  <br/> |[[LineCap] セル ([Line Format] セクション)](linecap-cell-line-format-section.md) <br/> |
|Linecolor]  <br/> |図形の線の色を指定します。  <br/> |[[LineColor] セル ([Line Format] セクション)](linecolor-cell-line-format-section.md) <br/> |
|[Linecolortrans]  <br/> |図形の線の色の透過性レベルを指定します。  <br/> |[[LineColorTrans] セル ([Line Format] セクション)](linecolortrans-cell-line-format-section.md) <br/> |
|[Linegradientangle]  <br/> |線形グラデーションの線のグラデーションの角度を、0 ~ 359.9 度の角度で指定します。  <br/> |[[Linegradientangle] セル (グラデーションのプロパティ] セクション)](linegradientangle-cell-gradient-properties-section.md) <br/> |
|[Linegradientdir]  <br/> |線のグラデーションの方向を決定します。 グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。  <br/> |[[Linegradientdir] セル (グラデーションのプロパティ] セクション)](linegradientdir-cell-gradient-properties-section.md) <br/> |
|[Linegradientenabled]  <br/> |線または図形の境界線で線のグラデーションを有効にするかどうかを決定します。  <br/> |[[Linegradientenabled] セル (グラデーションのプロパティ] セクション)](linegradientenabled-cell-gradient-properties-section.md) <br/> |
|[Linejumpcode]  <br/> |飛び越し点を表示するコネクタを指定します。  <br/> ||
|[Linejumpfactorx]  <br/> |[LineToLineX] セルの値を基準にして、ページ上にある水平方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。  <br/> |[[LineJumpFactorX] セル ([Page Layout] セクション)](linejumpfactorx-cell-page-layout-section.md) <br/> |
|[Linejumpfactory]  <br/> |[LineToLineY] セルの値を基準にして、ページ上にある垂直方向の動的コネクタの飛び越し点のサイズを決定します。このセルの値には、0 ～ 10 の値を使用できますが、0 ～ 1 の数値の使用をお勧めします。  <br/> |[[LineJumpFactorY] セル ([Page Layout] セクション)](linejumpfactory-cell-page-layout-section.md) <br/> |
|[Linejumpstyle]  <br/> |ローカルな飛び越し点のスタイルを持たない図面ページ上のすべてのコネクタに対して、飛び越し点のスタイルを指定します。  <br/> |[[LineJumpStyle] セル ([Page Layout] セクション)](linejumpstyle-cell-page-layout-section.md) <br/> |
|[Linepattern]  <br/> |図形の線の種類を指定します。[LinePattern] セルには、線の種類のコレクション内でインデックスとなっている数字を入力します。  <br/> |[[LinePattern] セル ([Line Format] セクション)](linepattern-cell-line-format-section.md) <br/> |
|[Linerouteext]  <br/> |図面ページにあるすべてのコネクタの既定の外観を指定します。  <br/> |[[LineRouteExt] セル ([Page Layout] セクション)](linerouteext-cell-page-layout-section.md) <br/> |
|Linetolinex]  <br/> |図面ページにあるすべてのコネクタ間の水平方向のクリアランスを指定します。  <br/> |[[LineToLineX] セル ([Page Layout] セクション)](linetolinex-cell-page-layout-section.md) <br/> |
|Linetoliney]  <br/> |図面ページにあるすべてのコネクタ間の垂直方向のクリアランスを指定します。  <br/> |[[LineToLineY] セル ([Page Layout] セクション)](linetoliney-cell-page-layout-section.md) <br/> |
|[Linetonodex]  <br/> |図面ページにあるすべてのコネクタと図形間の水平方向のクリアランスを指定します。  <br/> |[[LineToNodeX] セル ([Page Layout] セクション)](linetonodex-cell-page-layout-section.md) <br/> |
|[Linetonodey]  <br/> |図面ページにあるすべてのコネクタと図形間の垂直方向のクリアランスを指定します。  <br/> |[[LineToNodeY] セル ([Page Layout] セクション)](linetonodey-cell-page-layout-section.md) <br/> |
|LineWeight  <br/> |図形の線の太さを指定します。 線の太さを設定するには、有効な単位を使用して数値を入力します。  <br/> |[[LineWeight] セル ([Line Format] セクション)](lineweight-cell-line-format-section.md) <br/> |
|[Localizemerge]  <br/> |図形を図面間でコピーするときにローカライズするかどうかを指定します。  <br/> |[[LocalizeMerge] セル ([Miscellaneous] セクション)](localizemerge-cell-miscellaneous-section.md) <br/> |
|[Lockaspect]  <br/> |図形の縦横比をロックします。ロックすると、図形のサイズを変更するときに縦横比が維持されます。上下、左右のいずれか一方向だけサイズを変更することができなくなります。  <br/> |[[LockAspect] セル ([Protection] セクション)](lockaspect-cell-protection-section.md) <br/> |
|[Lockbegin]  <br/> |1-D 図形の始点 ([BeginX]、[BeginY]) を特定の位置にロックします。  <br/> |[[LockBegin] セル ([Protection] セクション)](lockbegin-cell-protection-section.md) <br/> |
|[Lockcalcwh]  <br/> |図形の選択範囲をロックして、頂点を編集した場合や、行の種類を [Geometry] セクションで変更した場合に再計算できないようにします。  <br/> |[[LockCalcWH] セル ([Protection] セクション)](lockcalcwh-cell-protection-section.md) <br/> |
|[Lockcrop]  <br/> |別のプログラムのオブジェクトをロックして、[トリミング ツール] を使用したトリミングができないようにします。  <br/> |[[LockCrop] セル ([Protection] セクション)](lockcrop-cell-protection-section.md) <br/> |
|[Lockcustprop]  <br/> |[図形データの定義] ダイアログ ボックス、または [図形データ] ウィンドウのショートカット メニューを使用して、ユーザー インターフェイス (UI) の図形データを追加、削除、または修正できるかどうかを判別します。  <br/> |[[LockCustProp] セル ([Protection] セクション)](lockcustprop-cell-protection-section.md) <br/> |
|[Lockdelete]  <br/> |図形をロックして、削除できないようにします。  <br/> |[[LockDelete] セル ([Protection] セクション)](lockdelete-cell-protection-section.md) <br/> |
|[Lockend]  <br/> |1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。  <br/> |[[LockEnd] セル ([Protection] セクション)](lockend-cell-protection-section.md) <br/> |
|[Lockformat]  <br/> |図形の書式設定をロックして、変更できないようにします。  <br/> |[[LockFormat] セル ([Protection] セクション)](lockformat-cell-protection-section.md) <br/> |
|[Lockfromgroupformat]  <br/> |グループ図形の書式設定の変更がサブ図形に反映されないようにしながら、選択したサブ図形の書式を直接設定できるようにします。 [LockFromGroupFormat] セルの値は、[保護] ダイアログ ボックスにある [グループ書式設定を適用不可にする] チェック ボックスの設定に対応します。  <br/> |[[LockFromGroupFormat] セル ([保護] セクション)](lockfromgroupformat-cell-protection-section.md) <br/> |
|[Lockgroup]  <br/> |グループをロックして、グループを解除できないようにします。  <br/> |[[LockGroup] セル ([Protection] セクション)](lockgroup-cell-protection-section.md) <br/> |
|[Lockheight]  <br/> |図形の高さをロックします。ロックすると、図形のサイズを変更しても高さは変更されません。  <br/> |[[LockHeight] セル ([Protection] セクション)](lockheight-cell-protection-section.md) <br/> |
|[Lockmovex]  <br/> |図形の水平位置をロックします。ロックすると、図形は水平方向に移動できなくなります。  <br/> |[[LockMoveX] セル ([Protection] セクション)](lockmovex-cell-protection-section.md) <br/> |
|[Lockmovey]  <br/> |図形の垂直位置をロックします。ロックすると、図形は垂直方向に移動できなくなります。  <br/> |[[LockMoveY] セル ([Protection] セクション)](lockmovey-cell-protection-section.md) <br/> |
|[Lockpreview]  <br/> |図面を保存するたびにプレビューを保存するかどうかを指定します。  <br/> |[[LockPreview] セル ([Document Properties] セクション)](lockpreview-cell-document-properties-section.md) <br/> |
|[Lockreplace]  <br/> |図形を置換操作に使用できるかどうか (ターゲット図形または置換後の図形のいずれかとして) を示します。  <br/> |[[LockReplace] セル ([Protection] セクション)](lockreplace-cell-protection-section.md) <br/> |
|[Lockrotate]  <br/> |2 次元図形をロックして、回転ハンドル、[左へ 90 度回転] コマンド、[右へ 90 度回転] コマンドによる回転操作ができないようにします。  <br/> |[[LockRotate] セル ([Protection] セクション)](lockrotate-cell-protection-section.md) <br/> |
|[Lockselect]  <br/> |図形の選択操作ができないようにします。  <br/> |[[LockSelect] セル ([Protection] セクション)](lockselect-cell-protection-section.md) <br/> |
|[Locktextedit]  <br/> |図形のテキストをロックして、編集できないようにします。  <br/> |[[LockTextEdit] セル ([Protection] セクション)](locktextedit-cell-protection-section.md) <br/> |
|[Lockthemecolors]  <br/> |テーマの色が図形に適用されないようにします。 [LockThemeColors] セルの値は、[保護] ダイアログ ボックスの [テーマの色を適用不可にする] チェックボックスの設定に対応します。  <br/> |[[Lockthemecolors] セル (Protection セクション)](lockthemecolors-cell-protection-section.md) <br/> |
|[Lockthemeconnectors]  <br/> |[テーマのプロパティ] 行の [ConnectorsSchemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。 ユーザーがシェイプシートのこの値を手動で変更することは防げません。  <br/> |[[Lockthemeconnectors] セル (Protection セクション)](lockthemeconnectors-cell-protection-section.md) <br/> |
|[Lockthemeeffects]  <br/> |[保護] ダイアログボックスの [テーマの効果] チェックボックスの設定に対応しています。  <br/> |[[Lockthemeeffects] セル (Protection セクション)](lockthemeeffects-cell-protection-section.md) <br/> |
|[Lockthemefonts]  <br/> |新しいテーマを適用することで、[Theme Properties] 行の [FontIndex] セルが変更されないようにします。 ユーザーがシェイプシートのこの値を手動で変更することは防げません。  <br/> |[[Lockthemefonts] セル (Protection セクション)](lockthemefonts-cell-protection-section.md) <br/> |
|[Lockthemeindex]  <br/> |[テーマのプロパティ] 行の [ThemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。 ユーザーがシェイプシートのこの値を手動で変更することは防げません。  <br/> |[[Lockthemeindex] セル (Protection セクション)](lockthemeindex-cell-protection-section.md) <br/> |
|[Lockvariation]  <br/> |ページまたは図形に適用するテーマのバリエーションを変更できるかどうかを、ブール演算型で決定します。  <br/> |[[LockVariation] セル ([保護] セクション)](lockvariation-cell-protection-section.md) <br/> |
|[Lockvtxedit]  <br/> |図形の頂点をロックします。ロックすると、頂点を編集できなくなります。  <br/> |[[LockVtxEdit] セル ([Protection] セクション)](lockvtxedit-cell-protection-section.md) <br/> |
|[Lockwidth]  <br/> |図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。  <br/> |[[LockWidth] セル ([Protection] セクション)](lockwidth-cell-protection-section.md) <br/> |
|[Locpinx]  <br/> |図形の原点を基準にしたときの、図形の Pin (回転の中心) の x 座標を表します。 [Locpinx] を決定するための既定の数式は\*次のとおりです。 = Width 0.5。  <br/> |[[LocPinX] セル ([Shape Transform] セクション)](locpinx-cell-shape-transform-section.md) <br/> |
|LockPinY  <br/> |図形の原点を基準にしたときの、図形の Pin (回転の中心) の y 座標を表します。 [Locpiny] を決定するための既定の数式は\* 、高さ0.5 です。  <br/> |[[LocPinY] セル ([Shape Transform] セクション)](locpiny-cell-shape-transform-section.md) <br/> |
|[Noalignbox]  <br/> |選択した図形の選択範囲の表示/非表示を切り替えます。  <br/> |[[NoAlignBox] セル ([Miscellaneous] セクション)](noalignbox-cell-miscellaneous-section.md) <br/> |
|[Nocoauth]  <br/> |共同編集セッションで、SharePoint 2013 サーバーまたは Microsoft OneDrive に格納されているドキュメントを複数の作成者が同時に編集できるようにするかどうかを設定します。  <br/> |[[NoCoauth] セル ([Document Properties] セクション)](nocoauth-cell-document-properties-section.md) <br/> |
|[Noctlhandles]  <br/> |図形を選択したときにコントロールハンドルが表示されないようにします。  <br/> |[[NoCtlHandles] セル ([Miscellaneous] セクション)](noctlhandles-cell-miscellaneous-section.md) <br/> |
|[Nolivedynamics]  <br/> |図形を操作するときに、図形のサイズを動的に変更したり、回転させるかどうかを指定します。  <br/> |[[NoLiveDynamics] セル ([Miscellaneous] セクション)](nolivedynamics-cell-miscellaneous-section.md) <br/> |
|印字  <br/> |選択した図形の印刷のオン/オフを切り替えます。  <br/> |[[NonPrinting] セル ([Miscellaneous] セクション)](nonprinting-cell-miscellaneous-section.md) <br/> |
|[Noobjhandles]  <br/> |選択した図形の選択ハンドルの表示/非表示を切り替えます。  <br/> |[[NoObjHandles] セル ([Miscellaneous] セクション)](noobjhandles-cell-miscellaneous-section.md) <br/> |
|NoProofing  <br/> |スペルを自動的に修正するかどうか、および選択した図形に対してスペルミスを表示するかどうかを決定します。  <br/> ||
|[Objtype]  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図面上のオブジェクトが配置可能かどうか、または迂回可能かどうかを指定します。  <br/> |[[ObjType] セル ([Miscellaneous] セクション)](objtype-cell-miscellaneous-section.md) <br/> |
|OnPage  <br/> |特定のプリンター ページ番号に図面を印刷するかどうかを示します。  <br/> |[[OnPage] セル ([Print Properties] セクション)](onpage-cell-print-properties-section.md) <br/> |
|OutputFormat  <br/> |図面の出力形式を指定します。 図面ページは、通常は印刷用に形式が設定されていますが (既定値)、他の出力形式を選択することもできます。  <br/> |[[OutputFormat] セル ([Document Properties] セクション)](outputformat-cell-document-properties-section.md) <br/> |
|[Pagebottommargin]  <br/> |印刷ページの下余白を指定します。  <br/> |[[PageBottomMargin] セル ([Print Properties] セクション)](pagebottommargin-cell-print-properties-section.md) <br/> |
|PageHeight  <br/> |図面単位で表した印刷ページの高さを指定します。  <br/> |[[PageHeight] セル ([Page Properties] セクション)](pageheight-cell-page-properties-section.md) <br/> |
|[Pageleftmargin]  <br/> |印刷ページの左余白を指定します。  <br/> |[[PageLeftMargin] セル ([Print Properties] セクション)](pageleftmargin-cell-print-properties-section.md) <br/> |
|[Pagelinejumpdirx]  <br/> |図面ページ上にある水平方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。  <br/> |[[PageLineJumpDirX] セル ([Page Layout] セクション)](pagelinejumpdirx-cell-page-layout-section.md) <br/> |
|[Pagelinejumpdiry]  <br/> |図面ページ上にある垂直方向の動的コネクタに対して、固有の飛び越し点の方向を適用していない場合、そのコネクタに表示される飛び越し点の方向を指定します。  <br/> |[[PageLineJumpDirY] セル ([Page Layout] セクション)](pagelinejumpdiry-cell-page-layout-section.md) <br/> |
|[Pagelockduplicate]  <br/> |ページを複製できるかどうかを、ブール演算型で決定します。  <br/> |[[PageLockDuplicate] セル ([Page Properties] セクション)](pagelockduplicate-cell-page-properties-section.md) <br/> |
|[Pagelockreplace]  <br/> |このページで [図形の置換] ボタンを無効にするかどうかを示します。  <br/> |[[PageLockReplace] セル ([Page Properties] セクション)](pagelockreplace-cell-page-properties-section.md) <br/> |
|[Pagerightmargin]  <br/> |印刷ページの右余白を指定します。  <br/> |[[PageRightMargin] セル ([Print Properties] セクション)](pagerightmargin-cell-print-properties-section.md) <br/> |
|[Pagescale]  <br/> |現在の図面縮尺でページ単位の値を指定します。ページの図面縮尺は、[DrawingScale] セルに表示される図面単位に対して [PageScale] セルに表示されるページ単位の比率です。  <br/> |[[PageScale] セル ([Page Properties] セクション)](pagescale-cell-page-properties-section.md) <br/> |
|[Pageshapesplit]  <br/> |ページの図形が自動的に分割されるかどうかを示します。  <br/> |[[PageShapeSplit] セル ([Page Layout] セクション)](pageshapesplit-cell-page-layout-section.md) <br/> |
|[Pagesx]  <br/> |図面ページに左右を揃えるプリンター ページの番号を指定します。  <br/> |[[PagesX] セル ([Print Properties] セクション)](pagesx-cell-print-properties-section.md) <br/> |
|[Pagesy]  <br/> |図面ページに上下を揃えるプリンター ページの番号を指定します。  <br/> |[[PagesY] セル ([Print Properties] セクション)](pagesy-cell-print-properties-section.md) <br/> |
|[Pagetopmargin]  <br/> |印刷ページの上余白を指定します。  <br/> |[[PageTopMargin] セル ([Print Properties] セクション)](pagetopmargin-cell-print-properties-section.md) <br/> |
|PageWidth  <br/> |印刷ページの幅を図面単位で指定します。  <br/> |[[PageWidth] セル ([Page Properties] セクション)](pagewidth-cell-page-properties-section.md) <br/> |
|[Paperkind]  <br/> |ページを印刷する用紙の種類を指定します。  <br/> |[[PaperKind] セル ([Print Properties] セクション)](paperkind-cell-print-properties-section.md) <br/> |
|PaperSource  <br/> |用紙の給紙方法を指定します。  <br/> |[[PaperSource] セル ([PrintProperties] セクション)](papersource-cell-printproperties-section.md) <br/> |
|Perspective  <br/> |遠近の回転の遠近の角度を指定します (0 ~ 359.9)。  <br/> |[透視セル (3-d 回転のプロパティセクション)](perspective-cell-3-d-rotation-properties-section.md) <br/> |
|[Pinx]  <br/> |親図形の原点を基準にしたときの、図形の Pin (回転の中心) の x 座標を表します。  <br/> |[[PinX] セル ([Shape Transform] セクション)](pinx-cell-shape-transform-section.md) <br/> |
|PinY  <br/> |親図形の原点を基準にしたときの、図形の Pin (回転の中心) の y 座標を表します。  <br/> |[[PinY] セル ([Shape Transform] セクション)](piny-cell-shape-transform-section.md) <br/> |
|[Placedepth]  <br/> |レイアウトを作成する前に図面を分析する方法を指定します。また、レイアウトの種類も指定します。  <br/> |[[PlaceDepth] セル ([Page Layout] セクション)](placedepth-cell-page-layout-section.md) <br/> |
|[Placeflip]  <br/> |[レイアウトの構成] ダイアログ ボックスを使用するときに、配置可能な図形をページ上で反転または回転する方法を指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[PlaceFlip] セル ([Page Layout] セクション)](placeflip-cell-page-layout-section.md) <br/> |
|[Placestyle]  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図形をページ上にどのように配置するかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[「Place Style」セル (「ページレイアウト」セクション)](placestyle-cell-page-layout-section.md) <br/> |
|[Plowcode]  <br/> |図面ページで、配置可能な図形を別の配置可能な図形の近くにドロップしたときに、これらの図形を移動して遠ざけるかどうかを指定します。  <br/> |[[PlowCode] セル ([Page Layout] セクション)](plowcode-cell-page-layout-section.md) <br/> |
|[Previewquality]  <br/> |図面プレビューの質がドラフト レベルであるか、詳細レベルであるかを指定します。  <br/> |[[PreviewQuality] セル ([Document Properties] セクション)](previewquality-cell-document-properties-section.md) <br/> |
|[Previewscope]  <br/> |図面にプレビューを含めるかどうかを指定します。図面にプレビューを含める場合は、プレビューに表示するページを指定します (最初のページのみ、または図面のすべてのページ)。  <br/> |[[PreviewScope] セル ([Document Properties] セクション)](previewscope-cell-document-properties-section.md) <br/> |
|[Printgrid]  <br/> |図面ページの印刷時にグリッドを印刷するかどうかを指定します。  <br/> |[[PrintGrid] セル ([Print Properties] セクション)](printgrid-cell-print-properties-section.md) <br/> |
|[Printpageorientation]  <br/> |ページの印刷方向を、縦向きにするか横向きにするかを指定します。  <br/> |[[PrintPageOrientation] セル ([Print Properties] セクション)](printpageorientation-cell-print-properties-section.md) <br/> |
|[Quickstyleeffectsmatrix]  <br/> |アクティブなテーマから図形を継承するクイック スタイル効果を、0 から 6 の整数で決定します。  <br/> ||
|[Quickstylefillcolor]  <br/> |図形の塗りつぶしに使用するテーマの色を、0から7の整数で指定します。  <br/> |[[Quickstylefillcolor] セル (クイックスタイルセクション)](quickstylefillcolor-cell-quick-style-section.md) <br/> |
|[Quickstylefillmatrix]  <br/> |使用中のテーマから図形を継承したスタイルをクイックスタイルで塗りつぶすかどうかを、0 から 6 の整数で決定します。  <br/> |[クイックスタイルの Fillmatrix セル (クイックスタイルセクション)](quickstylefillmatrix-cell-quick-style-section.md) <br/> |
|[Quickstylefontcolor]  <br/> |図形のテキストがアクティブなテーマから継承するクイックスタイルのフォントの色を、0-1 からの整数で指定します。  <br/> |[クイックスタイル Fontcolor セル (クイックスタイルセクション)](quickstylefontcolor-cell-quick-style-section.md) <br/> |
|[Quickstylefontmatrix]  <br/> |各クイックスタイルのフォントのスタイルを、1 ~ 6 の整数で指定します。  <br/> |[クイックスタイルの Fontmatrix セル (クイックスタイルのセクション)](quickstylefontmatrix-cell-quick-style-section.md) <br/> |
|[Quickstylelinecolor]  <br/> |図形の線が使用するテーマの色を、0から7の整数で指定します。  <br/> |[[Quickstylelinecolor] セル (クイックスタイルセクション)](quickstylelinecolor-cell-quick-style-section.md) <br/> |
|[Quickstylelinematrix]  <br/> |図形が継承するクイックスタイルの線のスタイルを、0-6 からの整数で指定します。  <br/> |[[Quickstylelinematrix] セル (クイックスタイルセクション)](quickstylelinematrix-cell-quick-style-section.md) <br/> |
|[Quickstyleshadowcolor]  <br/> |図形の影に使用するテーマの色を、0から7の整数で指定します。  <br/> |[[Quickstyleshadowcolor] セル (クイックスタイルセクション)](quickstyleshadowcolor-cell-quick-style-section.md) <br/> |
|[Quickstyletype]  <br/> |図形が継承するクイックスタイルの種類 (2 次元、1次元、またはコネクタ) を指定します。  <br/> |[クイックスタイルの Type セル (クイックスタイルセクション)](quickstyletype-cell-quick-style-section.md) <br/> |
|[Quickstylevariation]  <br/> |テーマが設定された図の背景に対して、図形のテキスト、線、塗りつぶしの色を表示します。  <br/> ||
|[Reflectionblur]  <br/> |図形の反射のぼかしの量を 0.0 ~ 100.0 のポイント単位で指定します。  <br/> |[[Reflectionblur] セル (その他の効果のプロパティセクション)](reflectionblur-cell-additional-effect-properties-section.md) <br/> |
|[Reflectiondist]  <br/> |反射を図形からオフセットする距離を 0.0 ~ 100.0 の範囲で指定します。  <br/> |[[Reflectiondist] セル (その他の効果のプロパティセクション)](reflectiondist-cell-additional-effect-properties-section.md) <br/> |
|[Reflectionsize]  <br/> |図形を基準にした反射のサイズを、0.0 ~ 100.0% の割合で指定します。 [Reflectionsize] セルの値が 0% の図形には反射がありません。100% の値を指定すると、図形の完全なミラーイメージが表示されます。  <br/> |[[Reflectionsize] セル (その他の効果のプロパティセクション)](reflectionsize-cell-additional-effect-properties-section.md) <br/> |
|[Reflectiontrans]  <br/> |反射の透明度を 0 ~ 100% の割合で指定します。  <br/> |[[Reflectiontrans] セル (その他の効果のプロパティセクション)](reflectiontrans-cell-additional-effect-properties-section.md) <br/> |
|リレーションシップ  <br/> |コンテナー、リスト、引き出し、および図形どうしの関係を格納します。  <br/> |[リレーションシップセル (Shape Layout セクション)](relationships-cell-shape-layout-section.md) <br/> |
|[Replacecopycells]  <br/> |図形の置換操作中に、古い図形から置換後の図形にコピーされるシェイプシート内のセル一覧を示します。  <br/> |[[Replacecopycells] セル (図形の動作の変更] セクション)](replacecopycells-cell-change-shape-behavior-section.md) <br/> |
|[Replacelockformat]  <br/> |マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。 マスター シェイプの [ReplaceLockFormat] セルが TRUE (1) に設定されている場合、マスターの書式設定値は、マスターによって置き換えられる図形の対応する値すべてに優先します。  <br/> |[[ReplaceLockFormat] セル ([図形の動作の変更] セクション)](replacelockformat-cell-change-shape-behavior-section.md) <br/> |
|[Replacelockshapedata]  <br/> |マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。 ReplaceLockShapeData は、マスター シェイプの図形データが、置換される図形の図形データすべてに優先するかどうかを決定します。  <br/> |[[Replacelock図形データ] セル ([図形動作の変更] セクション)](replacelockshapedata-cell-change-shape-behavior-section.md) <br/> |
|[Replacelocktext]  <br/> |マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。 ReplaceLockText は、マスターに表示されるテキストが、置換される図形のテキストに優先するかを決定します。  <br/> |[[ReplaceLockText] セル ([図形の動作の変更] セクション)](replacelocktext-cell-change-shape-behavior-section.md) <br/> |
|[Resizemode]  <br/> |図形に対して現在設定されているサイズ変更の動作の方法を示します。  <br/> |[[ResizeMode] セル ([Shape Transform] セクション)](resizemode-cell-shape-transform-section.md) <br/> |
|[Resizepage]  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトした後で、図面が中心に位置するようにページを拡大するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[ResizePage] セル ([Page Layout] セクション)](resizepage-cell-page-layout-section.md) <br/> |
|RightMargin  <br/> |テキスト ブロックの右の枠線と、そのブロックに含まれるテキストとの間隔を指定します。 既定値は 0.1 インチです。  <br/> |[[RightMargin] セル ([Text Block Format] セクション)](rightmargin-cell-text-block-format-section.md) <br/> |
|[Rotategradientwithshape]  <br/> |塗りつぶしのグラデーションが 2D 回転で図形に合わせて回転するかどうかを、ブール演算型で決定します。  <br/> |[[Rotategradientwithshape] セル (グラデーションのプロパティ] セクション)](rotategradientwithshape-cell-gradient-properties-section.md) <br/> |
|RotationType  <br/> |図形が並行回転、視点回転、または斜め回転に従って回転するかどうかを、0 から 6 までの整数で決定します。  <br/> |[RotationType セル (3-d 回転プロパティセクション)](rotationtype-cell-3-d-rotation-properties-section.md) <br/> |
|[Rotationxangle]  <br/> |X 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。  <br/> |[[Rotationxangle] セル (3-d 回転プロパティセクション)](rotationxangle-cell-3-d-rotation-properties-section.md) <br/> |
|[Rotationyangle]  <br/> |Y 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。  <br/> |[[Rotationyangle] セル (3-d 回転プロパティセクション)](rotationyangle-cell-3-d-rotation-properties-section.md) <br/> |
|[Rotationzangle]  <br/> |Z 軸に沿った回転角度を、° (0.0 ~ 359.9) で指定します。  <br/> |[[Rotationzangle] セル (3-d 回転プロパティセクション)](rotationzangle-cell-3-d-rotation-properties-section.md) <br/> |
|丸めの方法  <br/> |1 つのパス上で接する 2 つの連続したセグメントに適用される、円弧の半径を示します。たとえば、このセルを使用すると、四角形の角を丸くできます。丸みを設定するには、値と単位を入力します (数値と単位を組み合わせる)。  <br/> |[[Rounding] セル ([Line Format] セクション)](rounding-cell-line-format-section.md) <br/> |
|[Routestyle]  <br/> |ローカルな迂回方法を持たない図面ページ上のすべてのコネクタに対して、迂回方法と方向を指定します。  <br/> |[[RouteStyle] セル ([Page Layout] セクション)](routestyle-cell-page-layout-section.md) <br/> |
|ScaleX  <br/> |印刷ページの図面ページの倍率をパーセントで指定します。  <br/> |[[ScaleX] セル ([Print Properties] セクション)](scalex-cell-print-properties-section.md) <br/> |
|ScaleY  <br/> |印刷ページの図面ページの倍率をパーセントで指定します。  <br/> |[[ScaleY] セル ([Print Properties] セクション)](scaley-cell-print-properties-section.md) <br/> |
|[Selectmode]  <br/> |グループ図形とそのメンバーを選択する方法を指定します。  <br/> |[[SelectMode] セル ([Group Properties] セクション)](selectmode-cell-group-properties-section.md) <br/> |
|図形 (Fixedcode) セル  <br/> |配置可能な図形について、配置時の動作を指定します。  <br/> |[[ShapeFixedCode] セル ([Shape Layout] セクション)](shapefixedcode-cell-shape-layout-section.md) <br/> |
|図形のキーワード  <br/> |マスターシェイプに割り当てられている検索キーワードが含まれています。  <br/> ||
|[Shapepermeableplace]  <br/> |[レイアウトの構成] ダイアログ ボックスで図形をレイアウトするときに、配置可能な図形を図形の上部に配置するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[ShapePermeablePlace] セル ([Shape Layout] セクション)](shapepermeableplace-cell-shape-layout-section.md) <br/> |
|[Shapepermeablex]  <br/> |コネクタの接続経路が、配置可能な図形上を水平方向に通過するかどうかを指定します。  <br/> |[[ShapePermeableX] セル ([Shape Layout] セクション)](shapepermeablex-cell-shape-layout-section.md) <br/> |
|[Shapepermeabley]  <br/> |コネクタの接続経路が、配置可能な図形上を垂直方向に通過するかどうかを指定します。  <br/> |[[ShapePermeableY] セル ([Shape Layout] セクション)](shapepermeabley-cell-shape-layout-section.md) <br/> |
|[Shapeplaceflip]  <br/> |[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、配置可能な図形をページ上で反転および回転する方法、またはそのいずれかの方法を指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。  <br/> |[[ShapePlaceFlip] セル ([Shape Layout] セクション)](shapeplaceflip-cell-shape-layout-section.md) <br/> |
|[Shapeplacestyle]  <br/> |[レイアウトの構成] ダイアログボックスで図形をレイアウトするときに、図形をページに配置する方法を指定します ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。 VisCellIndices からレイアウト スタイルと整列の値を設定します。  <br/> |[「Shape Place Style] セル (Shape Layout セクション)](shapeplacestyle-cell-shape-layout-section.md) <br/> |
|[Shapeplowcode]  <br/> |図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。  <br/> |[[ShapePlowCode] セル ([Shape Layout] セクション)](shapeplowcode-cell-shape-layout-section.md) <br/> |
|[Shaperoutestyle]  <br/> |図面ページ上にある選択したコネクタの迂回方法と方向を指定します。  <br/> |[[ShapeRouteStyle] セル ([Shape Layout] セクション)](shaperoutestyle-cell-shape-layout-section.md) <br/> |
|[Shapeshdwblur]  <br/> |図形の影のぼかしのサイズをポイント単位 (0.00 ~ 100.00) で指定します。  <br/> |[[[Shapeshdwblur] セル ([塗りつぶしの書式設定] セクション)](shapeshdwblur-cell-fill-format-section.md) <br/> |
|[Shapeshdwobliqueangle]  <br/> |図形の斜体の影に角度を指定します。  <br/> |[[ShapeShdwObliqueAngle] セル ([Fill Format] セクション)](shapeshdwobliqueangle-cell-fill-format-section.md) <br/> |
|[Shapeshdwoffsetx]  <br/> |図形の影を図形から水平方向にオフセットする距離を、ページの単位で指定します。  <br/> |[[ShapeShdwOffsetX] セル ([Fill Format] セクション)](shapeshdwoffsetx-cell-fill-format-section.md) <br/> |
|[Shapeshdwoffsety]  <br/> |図形の影を図形から垂直方向にオフセットする距離を、ページの単位で指定します。  <br/> |[[ShapeShdwOffsetY] セル ([Fill Format] セクション)](shapeshdwoffsety-cell-fill-format-section.md) <br/> |
|[Shapeshdwscalefactor]  <br/> |図形の影を拡大または縮小できる割合を、パーセントで指定します。  <br/> |[[ShapeShdwScaleFactor] セル ([Fill Format] セクション)](shapeshdwscalefactor-cell-fill-format-section.md) <br/> |
|[Shapeshdwshow]  <br/> |図形に影を表示するかどうかを、0 から 2 の整数で決定します。  <br/> |[[[Shapeshdwshow] セル ([塗りつぶしの書式設定] セクション)](shapeshdwshow-cell-fill-format-section.md) <br/> |
|[Shapeshdwtype]  <br/> |図形の影の種類を指定します。  <br/> |[[ShapeShdwType] セル ([Fill Format] セクション)](shapeshdwtype-cell-fill-format-section.md) <br/> |
|[Shapesplit]  <br/> |この図形が、分割可能な図形を分割できるかどうかを示します。  <br/> |[[ShapeSplit] セル ([Shape Layout] セクション)](shapesplit-cell-shape-layout-section.md) <br/> |
|[Shapesplittable]  <br/> |この 1 次元図形が分割可能かどうかを示します。  <br/> |[[ShapeSplittable] セル ([Shape Layout] セクション)](shapesplittable-cell-shape-layout-section.md) <br/> |
|Sharpen  <br/> |ビットマップ イメージを鮮明にします。 既定値は 0% です。 イメージを鮮明にすると、隣接するピクセルのコントラストが上がり、イメージがはっきりと表示されます。  <br/> |[[Sharpen] セル ([Image Properties] セクション)](sharpen-cell-image-properties-section.md) <br/> |
|[Shdwforegnd]  <br/> |図形の影付きの塗りつぶしパターンに対して、前景 (ストローク) に使用する色を指定します。  <br/> |[[ShdwForegnd] セル ([Fill Format] セクション)](shdwforegnd-cell-fill-format-section.md) <br/> |
|[Shdwforegndtrans]  <br/> |図形の影に対して、塗りつぶしパターンの前景 (ストローク部分) に適用される色の透過性レベルを指定します。  <br/> |[[ShdwForegndTrans] セル ([Fill Format] セクション)](shdwforegndtrans-cell-fill-format-section.md) <br/> |
|[Shdwobliqueangle]  <br/> |既定のページの影の種類を適用したときの、斜めの方向を示す数字を指定します。  <br/> |[[ShdwObliqueAngle] セル ([Page Properties] セクション)](shdwobliqueangle-cell-page-properties-section.md) <br/> |
|[Shdwoffsetx]  <br/> |図形の影を図形から水平方向にオフセットする場合の距離を、ページの単位で指定します。  <br/> |[[ShdwOffsetX] セル ([Page Properties] セクション)](shdwoffsetx-cell-page-properties-section.md) <br/> |
|[Shdwoffsety]  <br/> |図形の影を図形から垂直方向にオフセットする場合の距離を、ページの単位で指定します。  <br/> |[[ShdwOffsetY] セル ([Page Properties] セクション)](shdwoffsety-cell-page-properties-section.md) <br/> |
|[Shdwpattern]  <br/> |図形の影の塗りつぶしパターンを指定します。  <br/> |[[ShdwPattern] セル ([Fill Format] セクション)](shdwpattern-cell-fill-format-section.md) <br/> |
|[Shdwscalefactor]  <br/> |図形の影を拡大または縮小する割合を、パーセントで指定します。  <br/> |[[ShdwScaleFactor] セル ([Page Properties] セクション)](shdwscalefactor-cell-page-properties-section.md) <br/> |
|[Shdwtype]  <br/> |ページの既定の影の種類を指定します。  <br/> |[[ShdwType] セル ([Page Properties] セクション)](shdwtype-cell-page-properties-section.md) <br/> |
|[Sketchamount]  <br/> |スケッチ効果に対するゆがみの量を、0 から 25 の整数で決定します。  <br/> |[[Sketchamount] セル (その他の効果のプロパティセクション)](sketchamount-cell-additional-effect-properties-section.md) <br/> |
|[Sketchenabled]  <br/> |図形にスケッチ効果を表示するかどうかを、ブール型 (Boolean) の値で指定します。  <br/> |[[Sketchenabled] セル (その他の効果のプロパティセクション)](sketchenabled-cell-additional-effect-properties-section.md) <br/> |
|[Sketchfillchange]  <br/> |スケッチ効果を使用するときに、図形の座標からの図形の塗りつぶしのランダム度を指定します。この値は、セクションの長さに対する割合として設定されます。 [Sketchfillchange] セルの値が 0% に設定されている場合、図形の塗りつぶしの境界図形は図形の座標に一致します。 値が 100% の場合、図形の塗りつぶしの境界ジオメトリは図形のジオメトリに沿っていません。  <br/> |[[Sketchfillchange] セル (その他の効果のプロパティセクション)](sketchfillchange-cell-additional-effect-properties-section.md) <br/> |
|[Sketchlinechange]  <br/> |スケッチ効果を使用するときに、図形の線のランダム化の量を、セクションの長さに対する割合として指定します。 [Sketchlinechange] セルの値が 0% に設定されている場合、図形の線のジオメトリは図形の図形座標と一致します。 値が 100% の場合、図形の線のジオメトリは図形のジオメトリに沿っていません。  <br/> |[[Sketchlinechange] セル (その他の効果のプロパティセクション)](sketchlinechange-cell-additional-effect-properties-section.md) <br/> |
|[Sketchlineweight]  <br/> |スケッチ効果の結果として、線の太さに追加された厚みを、0 から 50 のポイントで決定します。 [Sketchlineweight] セルの値が大きくなるにつれて、図形の線の太さが上がります。  <br/> |[[Sketchlineweight] セル (その他の効果のプロパティセクション)](sketchlineweight-cell-additional-effect-properties-section.md) <br/> |
|[Sketchseed]  <br/> |スケッチ効果の図形座標を決定するために使用されるランダム化の値を、正の整数で表します。 [SketchSeed] セルの値は、スケッチ効果を図形に適用するとき、ランダムで作成されます。  <br/> |[[Sketchseed] セル (その他の効果のプロパティセクション)](sketchseed-cell-additional-effect-properties-section.md) <br/> |
|[Softedgessize]  <br/> |ソフト エッジ効果のサイズを、0.00 から 100.00 までのポイントで決定します。 [SoftEdgesSize] セルの値が 0 の場合、図形にソフト エッジは適用されません。  <br/> |[[Softedgessize] セル (その他の効果のプロパティセクション)](softedgessize-cell-additional-effect-properties-section.md) <br/> |
|[Textbkgnd]  <br/> |図形のテキストの背景色を指定します。  <br/> |[[TextBkgnd] セル ([Text Block Format] セクション)](textbkgnd-cell-text-block-format-section.md) <br/> |
|[Textbkgndtrans]  <br/> |図形のテキスト ブロックの背景色に適用される透過性レベルを指定します。  <br/> |[[TextBkgndTrans] セル ([Text Block Format] セクション)](textbkgndtrans-cell-text-block-format-section.md) <br/> |
|TextDirection  <br/> |テキスト ブロック内にある文字の方向を指定します。  <br/> |[[TextDirection] セル ([Text Block Format] セクション)](textdirection-cell-text-block-format-section.md) <br/> |
|TheData  <br/> |将来使用するために予約されています。  <br/> |[[TheData] セル ([Events] セクション)](thedata-cell-events-section.md) <br/> |
|[Themeindex]  <br/> |ドキュメントに適用されている組み込みの Microsoft Visio テーマの列挙を整数として格納します。 新しいテーマをドキュメント用に選択した場合、ドキュメントの [ThemeIndex] セルとそこに格納されたすべてのページと図形が、組み込みテーマのインデックスを使用して更新されます。  <br/> |[[Themeindex] セル (テーマのプロパティセクション)](themeindex-cell-theme-properties-section.md) <br/> |
|[Thetext]  <br/> |図形のテキストまたはテキストの構成が変更されたときに評価されるイベント セルです。  <br/> |[[TheText] セル ([Events] セクション)](thetext-cell-events-section.md) <br/> |
|TopMargin  <br/> |テキスト ブロックの上の枠線から、そのブロックに含まれるテキストの最初の行までの間隔を指定します。既定値は 4.0000 ポイントです。この値は、図面の縮尺による影響を受けません。図面の縮尺を変更しても、上余白の長さは変わりません。  <br/> |[[TopMargin] セル ([Text Block Format] セクション)](topmargin-cell-text-block-format-section.md) <br/> |
|透明度  <br/> |図形のテキストの色に適用される透過性レベルを指定します。  <br/> |[[Transparency] セル ([Character] セクション)](transparency-cell-character-section.md) <br/> |
|透明度  <br/> |レイヤーの色の透過性レベルを指定します。  <br/> |[[Transparency] セル ([Image Properties] セクション)](transparency-cell-image-properties-section.md) <br/> |
|透明度  <br/> |レイヤーの色の透過性レベルを指定します。  <br/> |[[Transparency] セル ([Layers] セクション)](transparency-cell-layers-section.md) <br/> |
|[Txtangle]  <br/> |図形の x 軸を基準としたときの、テキスト ブロックの現在の回転角度を指定します。 既定値は 0°です。  <br/> |[[TxtAngle] セル ([Text Transform] セクション)](txtangle-cell-text-transform-section.md) <br/> |
|[Txtheight]  <br/> |テキスト ブロックの高さを指定します。 既定の数式は次のとおり\*です。 = 高さ1  <br/> |[[TxtHeight] セル ([Text Transform] セクション)](txtheight-cell-text-transform-section.md) <br/> |
|[Txtlocpinx]  <br/> |テキスト ブロックの原点を基準としたときの、テキスト ブロックの回転の中心となる x 座標を指定します。 既定の式は次のとおりです\* 。 = txtwidth 0.5 この数式は、テキストブロックの水平方向の中央に評価されます。  <br/> |[[TxtLocPinX] セル ([Text Transform] セクション)](txtlocpinx-cell-text-transform-section.md) <br/> |
|[Txtlocpiny]  <br/> |テキスト ブロックの原点を基準としたときの、テキスト ブロックの回転の中心となる y 座標を指定します。 既定の式は次のとおり\*です。 = [txtheight] 0.5  <br/> |[[TxtLocPinY] セル ([Text Transform] セクション)](txtlocpiny-cell-text-transform-section.md) <br/> |
|[Txtpinx]  <br/> |図形の原点を基準としたときの、テキスト ブロックの回転の中心となる x 座標を指定します。 既定の数式は次のとおり\*です。 = 幅0.5  <br/> |[[TxtPinX] セル ([Text Transform] セクション)](txtpinx-cell-text-transform-section.md) <br/> |
|[Txtpiny]  <br/> |図形の原点を基準としたときの、テキスト ブロックの回転の中心となる y 座標を指定します。 既定の式は次のとおり\*です。 = 高さ0.5  <br/> |[[TxtPinY] セル ([Text Transform] セクション)](txtpiny-cell-text-transform-section.md) <br/> |
|[Txtwidth]  <br/> |テキスト ブロックの幅を指定します。 既定の数式は次のとおり\*です。 = 幅1  <br/> |[[TxtWidth] セル ([Text Transform] セクション)](txtwidth-cell-text-transform-section.md) <br/> |
|[Uivisibility]  <br/> |ユーザー インターフェイス (UI) 内にページを表示するかどうかを指定します。  <br/> |[[UIVisibility] セル ([Page Properties] セクション)](uivisibility-cell-page-properties-section.md) <br/> |
|[Updatealignbox]  <br/> |コントロール ハンドルを移動するたびに選択範囲を再計算します。  <br/> |[[UpdateAlignBox] セル ([Miscellaneous] セクション)](updatealignbox-cell-miscellaneous-section.md) <br/> |
|[Usegroupgradient]  <br/> |図形が他の図形とグループ化されている場合、図形にグラデーションを適用するかどうかを、ブール演算型で決定します。 [UseGroupGradient] セルの値が影響するのは、図形の塗りつぶしのみです。  <br/> |[UseGroupGradient セル (Gradient Properties セクション)](usegroupgradient-cell-gradient-properties-section.md) <br/> |
|[Variationcolorindex]  <br/> |ページ上のアクティブなテーマのバリエーションの色のインデックスを整数で指定します。  <br/> |[[Variationcolorindex] セル (テーマのプロパティセクション)](variationcolorindex-cell-theme-properties-section.md) <br/> |
|[Variationstyleindex]  <br/> |ページ上のアクティブなテーマのバリエーションのスタイルインデックスを整数で指定します。  <br/> |[「バリエーションのインデックス」セル (「テーマのプロパティ」セクション)](variationstyleindex-cell-theme-properties-section.md) <br/> |
|[Verticalalign]  <br/> |テキスト ブロック内にあるテキストに対して、垂直方向の整列方法を指定します。  <br/> |[[VerticalAlign] セル ([Text Block Format] セクション)](verticalalign-cell-text-block-format-section.md) <br/> |
|[Viewmarkup]  <br/> |図面ウィンドウに校正履歴を表示するかどうかを指定します。  <br/> |[[ViewMarkup] セル ([Document Properties] セクション](viewmarkup-cell-document-properties-section.md) <br/> |
|[Walkpreference]  <br/> |1-D 図形をあいまいな位置に移動したときに、その図形の端点が、動的接着によって接着先の図形にある水平方向の接続ポイントに移動するのか、または垂直方向の接続ポイントに移動するのかを指定します。既定では、1-D 図形の始点と終点の両方とも水平方向の接続ポイントに移動します。  <br/> |[[WalkPreference] セル ([Glue Info] セクション)](walkpreference-cell-glue-info-section.md) <br/> |
|Width  <br/> |選択した図形の幅を図面の単位で表した値が表示されます。 1-d 図形の幅を決定する既定の数式は、= SQRT (([Endx]-[Beginx]) ^ 2 + ([Endy]-[Beginy]) ^ 2) です。  <br/> |[[Width] セル ([Shape Transform] セクション)](width-cell-shape-transform-section.md) <br/> |
|Xgriddensity]  <br/> |使用する水平方向のグリッドの種類を指定します。  <br/> |[[XGridDensity] セル&amp; ([ルーラーグリッド] セクション)](xgriddensity-cell-rulergrid-section.md) <br/> |
|[Xgridorigin]  <br/> |グリッド原点の水平方向の座標を指定します。  <br/> |[[XGridOrigin] セル&amp; ([ルーラ Grid] セクション)](xgridorigin-cell-rulergrid-section.md) <br/> |
|[Xgridspacing]  <br/> |固定グリッド (XGridDensity = 0) の水平線の間隔を指定します。  <br/> |[[XGridSpacing] セル&amp; ([ルーラーグリッド] セクション)](xgridspacing-cell-rulergrid-section.md) <br/> |
|[Xrulerdensity]  <br/> |ページのルーラーに対して、水平方向の小区分を指定します。  <br/> |[[XRulerDensity] セル&amp; ([ルーラーグリッド] セクション)](xrulerdensity-cell-rulergrid-section.md) <br/> |
|[Xrulerorigin]  <br/> |ページの x 軸のルーラーに対して、ゼロ点を指定します。  <br/> |[[XRulerOrigin] セル&amp; ([ルーラ Grid] セクション)](xrulerorigin-cell-rulergrid-section.md) <br/> |
|Ygriddensity]  <br/> |使用する垂直方向のグリッドの種類を指定します。  <br/> |[[YGridDensity] セル&amp; ([ルーラーグリッド] セクション)](ygriddensity-cell-rulergrid-section.md) <br/> |
|[Ygridorigin]  <br/> |グリッド原点の垂直方向の座標を指定します。  <br/> |[[YGridOrigin] セル&amp; ([ルーラーグリッド] セクション)](ygridorigin-cell-rulergrid-section.md) <br/> |
|[Ygridspacing]  <br/> |固定グリッド (YGridDensity = 0) の垂直線の間隔を指定します。  <br/> |[[YGridSpacing] セル&amp; ([ルーラーグリッド] セクション)](ygridspacing-cell-rulergrid-section.md) <br/> |
|[Yrulerdensity]  <br/> |ページのルーラーに対して、垂直方向の小区分を指定します。  <br/> |[[YRulerDensity] セル&amp; ([ルーラーグリッド] セクション)](yrulerdensity-cell-rulergrid-section.md) <br/> |
|[Yrulerorigin]  <br/> |ページの y 軸のルーラーに対して、ゼロ点を指定します。  <br/> |[[YRulerOrigin] セル&amp; ([ルーラーグリッド] セクション)](yrulerorigin-cell-rulergrid-section.md) <br/> |
   

