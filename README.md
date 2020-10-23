import { PIXI } from 'expo-pixi'
import { PixelRatio } from 'react-native'

import PanelSettings from './constants/PanelSettings'
import EditBoard from './models/objects/EditBoard'

export default class EditPanel {
  constructor(context, adjustDisplayObject, removeDisplayObject) {
    this.app = new PIXI.Application({
      context,
      backgroundColor: PanelSettings.backgroundColor
    });

    const board = new EditBoard(adjustDisplayObject, removeDisplayObject)
    const {width, height} = this.app.renderer
    board.containerWidth = width
    board.containerHeight = height
    board.appRenderer = this.app.renderer
    board.prepare()
    this.app.stage.addChild(board)
    this.board = board
  }
}

#- Father is  good and healthy here.
#- Mother and Sujong are treating disease yet.
#- They don't have baby yet.
#- HyongBom is doing original business.
#- All of family are worrying about you.
