# apimbds2021


L'API que utilisé pour recupérer les assignements depuis la base de données Mongo dans cloud ! 

C'est également celui que nous avions utilisé  au cours et modifié le fichier model/assignment.js :

resultat 

let mongoose = require("mongoose");
let Schema = mongoose.Schema;
var aggregatePaginate = require("mongoose-aggregate-paginate-v2");

let AssignmentSchema = Schema({
  id: Number,
  dateDeRendu: Date,
  nom: String,
  rendu: Boolean,
  matieres:Object,
  image:String,
  enseignant_nom:String,
  enseignant_photo:String,
  auteur:String,
  note:Number,
  remarques:String


});
AssignmentSchema.plugin(aggregatePaginate);

// C'est à travers ce modèle Mongoose qu'on pourra faire le CRUD
module.exports = mongoose.model("Assignment",AssignmentSchema);
