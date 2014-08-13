# Module Documentation

## Module Graphics.Canvas

### Types

    type Arc  = { end :: Number, start :: Number, r :: Number, cy :: Number, cx :: Number }

    data Canvas :: !

    data CanvasElement :: *

    data Context2D :: *

    type Rectangle  = { h :: Number, w :: Number, y :: Number, x :: Number }

    type ScaleTransform  = { scaleY :: Number, scaleX :: Number }

    type Transform  = { m32 :: Number, m31 :: Number, m22 :: Number, m21 :: Number, m12 :: Number, m11 :: Number }

    type TranslateTransform  = { translateY :: Number, translateX :: Number }


### Values

    arc :: forall eff. Context2D -> Arc -> Eff (canvas :: Canvas | eff) Context2D

    beginPath :: forall eff. Context2D -> Eff (canvas :: Canvas | eff) Context2D

    clearRect :: forall eff. Context2D -> Rectangle -> Eff (canvas :: Canvas | eff) Context2D

    clip :: forall eff. Context2D -> Eff (canvas :: Canvas | eff) Context2D

    fill :: forall eff. Context2D -> Eff (canvas :: Canvas | eff) Context2D

    fillPath :: forall eff a. Context2D -> Eff (canvas :: Canvas | eff) a -> Eff (canvas :: Canvas | eff) a

    fillRect :: forall eff. Context2D -> Rectangle -> Eff (canvas :: Canvas | eff) Context2D

    getCanvasElementById :: forall eff. String -> Eff (canvas :: Canvas | eff) CanvasElement

    getContext2D :: forall eff. CanvasElement -> Eff (canvas :: Canvas | eff) Context2D

    lineTo :: forall eff. Context2D -> Number -> Number -> Eff (canvas :: Canvas | eff) Context2D

    moveTo :: forall eff. Context2D -> Number -> Number -> Eff (canvas :: Canvas | eff) Context2D

    rect :: forall eff. Context2D -> Rectangle -> Eff (canvas :: Canvas | eff) Context2D

    restore :: forall eff. Context2D -> Eff (canvas :: Canvas | eff) Context2D

    rotate :: forall eff. Number -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    save :: forall eff. Context2D -> Eff (canvas :: Canvas | eff) Context2D

    scale :: forall eff. ScaleTransform -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    setFillStyle :: forall eff. String -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    setLineWidth :: forall eff. Number -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    setShadowBlur :: forall eff. Number -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    setShadowColor :: forall eff. String -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    setShadowOffsetX :: forall eff. Number -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    setShadowOffsetY :: forall eff. Number -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    setStrokeStyle :: forall eff. String -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    stroke :: forall eff. Context2D -> Eff (canvas :: Canvas | eff) Context2D

    strokePath :: forall eff a. Context2D -> Eff (canvas :: Canvas | eff) a -> Eff (canvas :: Canvas | eff) a

    strokeRect :: forall eff. Context2D -> Rectangle -> Eff (canvas :: Canvas | eff) Context2D

    transform :: forall eff. Transform -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    translate :: forall eff. TranslateTransform -> Context2D -> Eff (canvas :: Canvas | eff) Context2D

    withContext :: forall eff a. Context2D -> Eff (canvas :: Canvas | eff) a -> Eff (canvas :: Canvas | eff) a